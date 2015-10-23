These commands are tested on a debian-based distribution (Linux Mint 17 Cinnamon 64-bit). Please rephrase the following commands for your distribution.

### How to delete the Haskell toolchain:

 * I actually looked up all packages with ghc + haskell and removed them
   * `sudo apt-get purge ghc`
   * `sudo apt-get purge haskell-platform`
   * `sudo apt-get purge cabal`
   * `sudo apt-get purge cabal-install`
 * `sudo rm -rf ~/.cabal`
 * `sudo rm -rf ~/.ghc`
 * `sudo rm -rf ~/.stack`

### How to install the Haskell toolchain:

 * [official install guide](https://github.com/commercialhaskell/stack/blob/master/doc/GUIDE.md)
 * libtinfo missing? -> `sudo apt-get install libtinfo-dev`
 * want to use ghc / ghci without stack? -> add `$HOME/.stack/programs/x86_64-linux/ghc-<your-version>/bin/` to your `PATH`
 * want to use executables without `stack exec <executable>`? -> add `$HOME/.local/bin` to your `PATH`


### How to install the Haskell toolchain on CIP computers at the LMU

 * [download me](https://www.stackage.org/stack/linux-x86_64)
 * extract somewhere (e.g `~/Software/`)
 * rename the extracted folder to `stack`
 * updated your `~/.zsrhc` (if you use zsh) or create a file `~/.bashrc_local` and add the following line to it
   `export PATH=$PATH:$HOME/Software/stack`
 * run `stack setup`
 * you are good to go!