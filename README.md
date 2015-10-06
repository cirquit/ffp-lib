## How to delete Haskell / Cabal on Windows:

 * clean `C:\Documents and Settings\%USERNAME%\Application Data\cabal` (XP)
 * clean `C:\Program Files\Haskell Platform\lib`                       (XP)
 * clean `C:\Users\%USERNAME%\AppData\Roaming\cabal\bin`               (Win7 / Vista)
 * clean `C:\Users\%USERNAME%\AppData\Roaming\ghc`                     (Win7 / Vista)
 * clean `C:\Users\%USERNAME%\AppData\Roaming\ghci`                    (Win7 / Vista)
 * use the Haskell Platform uninstaller
 * delete MinGHC from wherever you unpacked it
 * update your PATH environment variable and remove deleted paths


## How to install Haskell on Windows (tested with Win7):

 * download latest release of [stack](https://github.com/commercialhaskell/stack/releases/tag/v0.1.5.0)
 * unpack into the folder of your choice - e.g `C:\Program Files\Haskell\`
 * rename the unpacked folder to `stack`
 * start Powershell / Command Prompt / Git Bash in the stack folder
 * execute `stack setup` - this can take some time
 * add the unpacked destination to the PATH environment variable e.g `C:\Program Files\Haskell\stack;`
 * add the executable destination to the PATH environemnt variable `C:\Users\%USERNAME%\AppData\Roaming\local\bin;`


## How to install Haskell on *nix systems:

 * [official install guide](https://github.com/commercialhaskell/stack/blob/master/doc/GUIDE.md)


### Tips and Help

 * [Editors](https://github.com/cirquit/ffp-lib/blob/master/editors.md)
 * [Stack information](https://github.com/cirquit/ffp-lib/blob/master/stack-info.md)
 * [Tips for working on a project](https://github.com/cirquit/ffp-lib/blob/master/tips.md)
 * [Stack & Yesod](https://github.com/cirquit/ffp-lib/blob/master/stack-n-yesod.md)