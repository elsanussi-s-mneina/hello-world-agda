
## Requirements:
 - Agda version 2.6.1
 - Agda standard library v1.3

### How to get Agda version 2.6.1
Go to the following web page: 

https://agda.readthedocs.io/en/v2.6.1/getting-started/installation.html

and follow the instructions

### How to get Agda standard library:
Follow the instructions at:

https://github.com/agda/agda-stdlib/blob/master/notes/installation-guide.md

## How to setup the Agda standard library so that the compiler will find it.
After you have downloaded and placed the uncompressed untarred version of the standard library in a location.

If you are in a Unix like system: Go to ~/.agda  folder.
If the folder does not exist, create the .agda folder.

Place a file named "libraries" there.

Put one line in that file. That line must be the path to the file whose extension is "agda-lib" located in the agda-stdlib-1.3 folder, which you recently downloaded.

~/.cabal/bin/agda-stdlib-1.3/standard-library.agda-lib


If you get stuck browse the documentation at 

https://agda.readthedocs.io/en/v2.6.1/tools/package-system.html

I wish it were easier, but it isn't because the Agda standard library does not ocome with Agda.

## How to compile:
Run the following line at the terminal, and press enter:

agda --compile src/hello-world.agda

Note: this will take much longer than usual. I think it is compiling the standard library also.

## How to run:

Type the following line at the terminal, and press enter. But first you must have compiled the program.

./src/hello-world

A message saying "hello world" should appear.


