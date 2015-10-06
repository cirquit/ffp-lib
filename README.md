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

## How to start:

 * `stack new <projectname>`
 * short explanation
   * app-dir is where the main entry point of your executable lies
   * src-dir is where the library lies
   * test-dir is where the tests lie
   * License is self-explainatory
   * Setup.hs is good practice, don't mind it for now
   * <projectname>.cabal is where all your dependencies are tracked, as well as other project information
   * stack.yaml is where e.g locally build packages are tracked
 * `stack build` installs your local library / executable
 * `stack test` runs the test-suite(s)
 * `stack exec <projectname>-exe` runs your local executable
 * if you use a library add it to the .cabal-file at the `build-depends` flag
 * if you use a library that's not in scope in the lts-build, add it to the `extra-deps` flag in the `stack.yaml` file
   * ```
     extra-deps:
     - my-lib-name-0.1.0.0
     ```
 




### Tips and Help

 * [Editors](https://github.com/cirquit/ffp-lib/blob/master/editors.md)
 * [Stack information](https://github.com/cirquit/ffp-lib/blob/master/stack-info.md)
 * [Tips for working on a project](https://github.com/cirquit/ffp-lib/blob/master/tips.md)
 * [Stack & Yesod](https://github.com/cirquit/ffp-lib/blob/master/stack-n-yesod.md)