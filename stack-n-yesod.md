### Stack & Yesod

If you want the automatized refresh on save feature + all yesod features you need the executable:

 * stack install yesod
 * stack install yesod-bin
 * stack install cabal-install
 * stack exec yesod init
 * cd <project-name>
 * stack init
 * stack exec yesod devel

If you want only the library:

 * stack install yesod
 * stack runghc <some-yesod-file.hs>

For examples / tutorials / the book - [link](http://www.yesodweb.com/)