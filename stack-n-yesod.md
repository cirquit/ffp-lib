### Stack & Yesod

If you want the automatized refresh on save feature + all yesod features you need the executable:

 * `stack install yesod`
 * `stack install yesod-bin`
 * `stack install cabal-install`
 * `stack exec yesod init`
 * `cd <project-name>`
 * `stack init`
 * `stack exec yesod devel`

If you want only the library:

 * `stack install yesod`
 * `stack runghc <some-yesod-file.hs>`

This doesn't work currently for yesod projects (tested with Win7):
 
 * `stack build` -> [link to stack overflow](http://stackoverflow.com/questions/31194891/haskell-stack-build-error-ghc-exe-could-not-execute)


My own examples from the last course - [link](https://github.com/cirquit/quizlearner/tree/master/resources/src)

For other examples / tutorials / the book - [link](http://www.yesodweb.com/)