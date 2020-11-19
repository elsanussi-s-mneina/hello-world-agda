
## Requirements:
 - Agda version 2.6.1
 - Agda standard library v1.3

## Quick instructions for Mac OS Catalina
Assuming you already installed brew, and cabal.
For information on Brew, see:
https://brew.sh/

For information on Cabal, see:
https://www.haskell.org/platform/ 


```
brew install agda
mkdir -p ~/.agda
echo /usr/local/lib/agda/standard-library.agda-lib >>~/.agda/libraries
echo standard-library >>~/.agda/defaults
cabal install --lib ieee754
```
Now you are ready to compile the code.


### How to get Agda version 2.6.1
Go to the following web page: 

https://agda.readthedocs.io/en/v2.6.1/getting-started/installation.html

and follow the instructions


### How to get Agda standard library:
Follow the instructions at:

https://github.com/agda/agda-stdlib/blob/master/notes/installation-guide.md

## How to setup the Agda standard library so that the compiler will find it.
After you have downloaded and placed the uncompressed untarred version of the standard library in a location.

See documentation at 

https://agda.readthedocs.io/en/v2.6.1/tools/package-system.html

I wish it were easier, but it isn't because the Agda standard library does not come with Agda.

## Troubleshooting the IEEE Numeric problem
If you encounter the following error when compiling:

```
s/Code/hello-world-agda/src/MAlonzo/RTE.hs:9:1: error:
    Could not find module ‘Numeric.IEEE’
    Use -v (or `:set -v` in ghci) to see a list of the files searched for.
  |
9 | import Numeric.IEEE ( IEEE(identicalIEEE, nan) )
  | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
```
You need to install the ieee754 library.
You can do so with the following command if cabal is installed.

`cabal install --lib ieee754`

## How to compile:
Run the following line at the terminal, and press enter:

agda --compile src/hello-world.agda

Note: this will take much longer than usual. I think it is compiling the standard library also.

## How to run:

Type the following line at the terminal, and press enter. But first you must have compiled the program.

./src/hello-world

A message saying "hello world" should appear.


