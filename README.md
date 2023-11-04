# agon-forth
Forth for Agon computer

## forth16

The `forth16` directory contains a 16-bit FORTH for Agon, to be run in Z-80 mode. This is not my development focus.

## forth24

The `forth24` directory contains a 24-bit FORTH for Agon, to be run in
eZ80 ADL mode. This can use all available RAM. Currently this has the
same feature set as `forth16` plus some extras, and will be further developed.

## fof (@jackokring)

The `fof` directory is under active development. It started as a clone of `forth16` and is being minimized and extrended
for use as a `*fof` command for including in the `mos` directory on the sdcard as `mos/fof.bin`. This of course limits
memory to 32kB and was the main reason to pick a 16-bit forth for this application.

The intent is a forth that builds in a similar manor, has reduce memory requirements, is actively developed
and will run almost all `forth15` and `forth24` source code.

The crazy hoops to go through to allow a 16-bit app to use 24-bit (double) `DOSCALL` so that it can load things in any memory.
It makes the code more compact though. The word `FREEMAX` might get you an extra 32kB if you `*load fof.bin` low.
Being 16-bit code, it will run low too. `XEXECUTE` will run 24-bit machine code and passes all the 16-bit registers
like all `CODE`/`END-CODE` expect. You may have to use `.SIS` for access. Return is by `RET .LIL` as usual.


