## How to delete Haskell / Cabal on Windows:

 * clean `C:\Documents and Settings\%USERNAME%\Application Data\cabal` (XP)
 * clean `C:\Program Files\Haskell Platform\lib`                       (XP)
 * clean `C:\Users\%USERNAME%\AppData\Roaming\cabal\bin`               (Win7 / Vista)
 * clean `C:\Users\%USERNAME%\AppData\Roaming\ghc`                     (Win7 / Vista)
 * clean `C:\Users\%USERNAME%\AppData\Roaming\ghci`                    (Win7 / Vista)
 * use the Haskell Platform uninstaller
 * delete MinGHC from wherever you unpacked it
 * update your PATH variable and remove deleted paths


## How to install Haskell on Windows (tested with Win7):

 * download latest release of [stack] (https://github.com/commercialhaskell/stack/releases/tag/v0.1.5.0)
 * unpack into the folder of your choice - e.g `C:\Program Files\Haskell\`
 * rename the unpacked folder to `stack`


## Editor (first two are highly customizable + nice highlighting):
 
 * [Sublime Text] (http://www.sublimetext.com/3)
   ** go to `Preferences -> Settings - User` and copy paste:
     ```
     {
      "draw_white_space_all": "all",
      "font_size": 11,  
      "tab_size": 2,
      "translate_tabs_to_spaces": true
     }
     ```
 * [Notepad++] (https://notepad-plus-plus.org/)
   ** go to `Settings -> Preferences -> Tab Settings` and check `Replace by space` and modify `Tab size` to 2
   ** if you are working with someone who is using a *nix-like system, go to `Settings -> Preferences -> New Document` and check `Format (Line ending)`to `UNIX/OSX`
 * vim - [nice plugin] (https://github.com/lukerandall/haskellmode-vim)
 * emacs
 * [or others] (https://wiki.haskell.org/IDEs)


### Nice perks for working with Haskell on Windows:

 * *nix like shell and git support - [Git4Win] (https://git-for-windows.github.io/)