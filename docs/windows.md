These are commands for multiple systems with differend previous state, you don't have to have every directory or installed programs. Just follow every step as far as possible.

### How to delete the Haskell toolchain:

 * clean `C:\Documents and Settings\%USERNAME%\Application Data\cabal` (XP)
 * clean `C:\Program Files\Haskell Platform\lib`                       (XP)
 * clean `C:\Users\%USERNAME%\AppData\Roaming\cabal\bin`               (Win7 / Vista)
 * clean `C:\Users\%USERNAME%\AppData\Roaming\ghc`                     (Win7 / Vista)
 * clean `C:\Users\%USERNAME%\AppData\Roaming\ghci`                    (Win7 / Vista)
 * use the *Haskell Platform* uninstaller
 * delete *MinGHC* from wherever you unpacked it
 * delete `stack` from whereever you unpacked it
 * update your `PATH` environment variable and remove deleted paths


### How to install Haskell on Windows (tested with Win7):

 * download latest release of [stack](https://github.com/commercialhaskell/stack/releases/tag/v0.1.5.0)
 * unpack into the folder of your choice - e.g `C:\Program Files\Haskell\`
 * rename the unpacked folder to `stack`
 * start *Powershell* / *Command Prompt* / *Git Bash* / *MSys2* in the stack folder
 * execute `stack setup` - this can take some time
 * add the unpacked destination to the `PATH` environment variable e.g `C:\Program Files\Haskell\stack;`
 * add the executable destination to the `PATH` environment variable `C:\Users\%USERNAME%\AppData\Roaming\local\bin;`
