## Learning haskell

- first project where I will read through [this awesome
  book](http://learnyouahaskell.com/).
- My approach: Reading through the description of the functions and then
  implementing my version to check against the code sample.
- Trying to get a basic understanding of haskell.

## install haskell toolchain
- if you don't have the haskell toolchain installed, run
```shell
curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh
```
to get ghcup and install the tools.

## semantics of my comments
- normally I use ="" for somewhat translations if I don't understand stuff.
- normally I use -> for links between topics or when I infer/conclude something.
  Somewhat late I noticed that -> will be pretty confusing since it is haskell
syntax. There it at some point (started with Typeclasses.ts) -> became --> to
differ from haskell syntax and semantic.

## play around with these functions
- Everything is stored under ./src/CodeBaseLibrary.hs.
- To execute the functions just open the haskell REPL and load the file.
```shell
ghci
ghci :l /src/CodeBaseLibrary
-- you can now use any function defined in the given file.
ghci map' (+1) [1..10]
ghci filter' even [1..10]
ghci filter' (\x -> (mod x 2) == 0) [1..10]
ghci zip' (filter' even  (map (+3) [1..10])) [200..]
ghci applyFuncTwice (+3) 2
```
- If you change code inside /src/CodeBaseLibrary and want to test it, just use
  :r /src/CodeBaseLibrary inside the repl to reload the file.


# compile haskell project using cabal
```shell
cabal build
cabal run
```

## where to get infos about haskell packages and implementations?
- I currently think [hoogle](https://hoogle.haskell.org/) is decent.
