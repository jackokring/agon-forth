# agon-forth
Forth for Agon computer

## forth16

The `forth16` directory contains a 16-bit FORTH for Agon, to be run in Z-80 mode. This is not a development focus.

## forth24

The `forth24` directory contains a 24-bit FORTH for Agon, to be run in
eZ80 ADL mode. This can use all available RAM. Currently this has the
same feature set as `forth16` plus some extras, and will be further developed.

## fof (@jackokring)

The `fof` directory is under active development. It started as a clone of `forth16` and is being minimized and extrended
for use as a `*fof` command for including in the `mos` directory on the sdcard as `mos/fof.bin`. This of course limits
memory to 32kB and was the main reason to pick a 16-bit forth for this application.

The intent is a forth that builds in a similar manor, has reduce memory requirements, is actively developed unlike `forth16`
and will run almost all `forth24` source code.

The crazy hoops to go through to allow a 16-bit app to use 24-bit `OSCALL` so that it can load things in any memory.

