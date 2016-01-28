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

This doesn't work under Win 7:
 
 * `stack build` -> [link to stack overflow](http://stackoverflow.com/questions/31194891/haskell-stack-build-error-ghc-exe-could-not-execute)


### Examples

 * my own examples from the last course - [link](https://github.com/cirquit/quizlearner/tree/master/resources/)
 * for other examples / tutorials / the book - [link](http://www.yesodweb.com/)

 * To run those minimal examples - `stack runghc <example.hs>`
 * To add handler via Yesod - `stack exec yesod add-handler`