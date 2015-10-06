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

 * download latest release of [stack](https://github.com/commercialhaskell/stack/releases/tag/v0.1.5.0)
 * unpack into the folder of your choice - e.g `C:\Program Files\Haskell\`
 * rename the unpacked folder to `stack`
 * run in Powershell / Command Prompt / Git Bash (in the stack folder) `stack build` - this can take some time
 * go to your environment variables and create/edit a PATH variable where you add the following line `C:\Program Files\Haskell\stack;C:\Users\Alex\AppData\Roaming\local\bin;`, or replace the first path with your unpacked stack folder


## How to install Haskell on debian-basted unix systems:

 * [official install guide](https://github.com/commercialhaskell/stack/blob/master/doc/GUIDE.md)

##### Working on a Haskell project with others:

 * try to use a style guide e.g [Chris Done's](https://github.com/chrisdone/haskell-style-guide)
 * use a version control system e.g git / svn
 * don't use tabs - **ever** (see editor preferences & style guide)
 * use .cabal-files to track dependencies


##### Stack related information:

 * [First steps, from blank system to a haskell project](https://github.com/commercialhaskell/stack/blob/master/doc/GUIDE.md)
 * [FAQ](https://github.com/commercialhaskell/stack/blob/master/doc/faq.md)
 * [YAML-Config](https://github.com/commercialhaskell/stack/blob/master/doc/yaml_configuration.md)
 * a list of useful commands used by stack
   * `stack runghc` == `runhaskell / runghc`
   * `stack install <pgkname>` == `cabal install <pgkname>`
   * `stack build` == `cabal build`
   * `stack ghci` == `ghci`
 * [using yesod with stack](http://www.yesodweb.com/blog/2015/06/stack-support-yesod-devel)

##### Editor (first two are highly customizable + nice highlighting):
 
 * [Sublime Text](http://www.sublimetext.com/3)
   * go to `Preferences -> Settings - User` and copy paste:
     ```
     {
      "draw_white_space_all": "all",
      "font_size": 11,  
      "tab_size": 2,
      "translate_tabs_to_spaces": true
     }
     ```
 * [Notepad++](https://notepad-plus-plus.org/)
   * go to `Settings -> Preferences -> Tab Settings` and check `Replace by space` and modify `Tab size` to 2
   * if you are working with someone who is using a *nix-like system, go to `Settings -> Preferences -> New Document` and check `Format (Line ending)`to `UNIX/OSX`
 * vim - [nice plugin](https://github.com/lukerandall/haskellmode-vim)
 * emacs
 * [or others](https://wiki.haskell.org/IDEs)


##### Nice perks for working with Haskell on Windows:

 * *nix like shell and git support - [Git4Win](https://git-for-windows.github.io/)
 * Powershell
   * `Win-Flag -> Search "Powershell"`
   * `Win-Flag -> Alle Programme -> Zubehör -> Windows Powershell`

