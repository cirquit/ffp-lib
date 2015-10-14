##### Basic Installation for GTK [link](https://wiki.haskell.org/Gtk2Hs/Installation)

#### GTK on Windows

 * precompiled binaries for pkg-config and dependencies - [link](http://ftp.gnome.org/pub/gnome/binaries/win32/dependencies/)
 * extended tutorial to install pkg-config on windows - [link](http://stackoverflow.com/questions/1710922/how-to-install-pkg-config-in-windows)
 * not working because of pkg-config & glib dependencies (Win)

#### GTK on Debian-based Unix

 * `sudo apt-get install libghc-gtk-dev` - install gtk
 * `stack new <projectname>`
 * `cd .. <projectname>`
 * edit the `<projectname>.cabal`
 ```
 executable <projectname>-exe
    hs-source-dirs:      app
    main-is:             Main.hs
    ghc-options:         -threaded -rtsopts -with-rtsopts=-N
    build-depends:       base
                       , <projectname>
                       , gtk
    default-language:    Haskell2010
 ```
   * edit `app/Main`
  ```Haskell
  module Main where

  import Graphics.UI.Gtk

  main :: IO ()
  main = do
     initGUI
     window <- windowNew
     widgetShowAll window
     onDestroy window mainQuit
     mainGUI
  ```
  * try `stack build`
  * libtinfo missing? -> `sudo apt-get install libtinfo-dev`
  * if it's installed but still not found, go to `/lib` and `/lib64` and create a link from `libtinfo.so.5` to `libtinfo.so` in the same directory
  * `stack build`
  * `stack exec <projectname>-exe`

#### Glade

 * `sudo apt-get install glade-gnome` - install glade for GTK+ 2
 * [Tutorials](https://github.com/gtk2hs/gtk2hs/tree/master/docs/tutorial/Tutorial_Port/Example_Code) (without glade)
 * There are no known tutorials for glade support (that I know of), BUT this rudimentary functionality should get you started

#### Basic how-to (installed glade + gtk + gtk-library):

(Main.hs and frame.glade are also uploaded in [this repository](https://github.com/cirquit/ffp-lib/blob/master/gtk-examples))

 * stack new
 * `cd <projectname>/app` and open `Main.hs`
 * copy this
  ```Haskell
  module Main where

  import Graphics.UI.Gtk
  import Graphics.UI.Gtk.Builder

  main :: IO ()
  main = do
     initGUI
     builder <- builderNew
     builderAddFromFile builder "frame.glade"
     window <- builderGetObject builder castToWindow "window1"
     widgetShowAll window
     onDestroy window mainQuit
     mainGUI
  ```
 * copy `frame.glade` into the main directory of your project (next to the `.cabal`-file)

   ```XML
   <?xml version="1.0" encoding="UTF-8"?>
   <interface>
     <requires lib="gtk+" version="2.24"/>
     <!-- interface-naming-policy project-wide -->
     <object class="GtkWindow" id="window1">
       <property name="can_focus">False</property>
       <property name="title" translatable="yes">My first glade powered program</property>
       <property name="default_width">250</property>
       <property name="default_height">250</property>
       <child>
         <object class="GtkLabel" id="label1">
           <property name="visible">True</property>
           <property name="can_focus">False</property>
           <property name="label" translatable="yes">Hello World - from Glade!</property>
         </object>
       </child>
     </object>
   </interface>
   ```
 * add `gtk` to your `<projectname.cabal` dependencies for the executable
 * `stack build`
 * `stack exec <projectname>-exe`