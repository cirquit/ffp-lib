##### Basic Installation for GTK [link](https://wiki.haskell.org/Gtk2Hs/Installation)

#### GTK on Windows

 * precompiled binaries for pkg-config and dependencies - [link](http://ftp.gnome.org/pub/gnome/binaries/win32/dependencies/)
 * extended tutorial to install pkg-config on windows - [link](http://stackoverflow.com/questions/1710922/how-to-install-pkg-config-in-windows)
 * not working because of pkg-config & glib dependencies (Win)

#### GTK on Debian-based Unix

 * `sudo apt-get install libghc-gtk-dev` - install gtk
 * `stack new <projectname>`
 * `cd .. <projectname>`
 * edit the <projectname>.cabal
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
  * `stack build`
  * edit `bin/Main`
  ```Haskell
  module Main where

  import Graphics.UI.Gtk
   
  main :: IO ()
  main = do
     initGUI
     window <- windowNew
     widgetShowAll window
     mainGUI
  ```
  * `stack exec <projectname>-exe`


**Glade** needs
 * `glib >=0.12.5.0 && <0.13`
 * `gtk >=0.12.5.0 && <0.13`
The next gtk-lib which is <0.13 is 0.12.5.7 and it needs
 * cairo: needed (>=0.12.5.3 && <0.13)
 * gio: needed (>=0.12.5 && <0.13)    
 * glib: needed (>=0.12.5.4 && <0.13) 
 * pango: needed (>=0.12.5.3 && <0.13)


