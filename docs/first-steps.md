## How to start:

 * `stack new <projectname>`
 * short explanation
   * `app-dir` is where the main entry point of your executable lies
   * `src-dir` is where the library lies
   * `test-dir` is where the tests lie
   * `License` is self-explainatory
   * `Setup.hs` is good practice, don't mind it for now
   * `<projectname>.cabal` is where all your dependencies are tracked, as well as other project information
   * `stack.yaml` is where e.g locally build packages are tracked
 * `stack build` installs your local library / executable
 * `stack test` runs the test-suite(s)
 * `stack exec <projectname>-exe` runs your local executable
 * if you use a library add it to the `<projectname>.cabal` file at the `build-depends` flag as such:

 ```
 library
  hs-source-dirs:      src
  exposed-modules:     Lib
  build-depends:       base >= 4.7 && < 5
                     , my-library ==0.1.0.0
 ```

 * if you use a library that's not in scope in the lts-resolver, add it to the `extra-deps` flag in the `stack.yaml` file as such:

 ```
 extra-deps:
   - my-lib-name-0.1.0.0
 ```
 * when in doubt or missing dependencies? `stack build` and read the error
