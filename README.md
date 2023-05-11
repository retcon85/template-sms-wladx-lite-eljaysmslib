# A very, very, very simple WLA-DX template for an SMS game based on library at https://github.com/lajohnston/smslib

## Quickstart

1. Either create a new repo using this one as a template from the github UI, use the `gh repo create` command line, or just clone this repo and manually rename / change git remotes etc.
2. Run `git submodule init`
3. Run `git submodule update`

The last two commands will populate the lib/smslib folder with the library.
Alternatively when you clone you could use the `--recurse-submodules` flag.

## Features

- Basic Makefile to build the project
- Example Hello World program from smslib's examples folder

## WLA-DX features non demonstrated

- Too numerous to mention!

## Prerequisites

### Using toolchain-sms Docker image (recommended)

See [here](https://github.com/retcon85/toolchain-sms/blob/main/README.md#usage) for instructions on pulling and using the image.

**Note:** this Docker image has currently only been tested under MacOS, although it would be expected to work under Linux also.

or

### Installing dependencies manually


- [WLA-DX](https://github.com/vhelin/wla-dx)
- [GNU Make](https://www.gnu.org/software/make/)

## Build instructions

1. Download and install prerequisites
1. Run `make` or `make build` to build a .sms file into the `build` folder
1. Read the docs at https://wla-dx.readthedocs.io/en/latest/index.html
1. Have fun

## Cleaning

Run `make clean` to clean the build

## Example program

The [example.s](https://github.com/retcon85/sms-template-lite/blob/main/src/example.s) file is a working program which flashes the background color at a rate of 60Hz (50Hz on a PAL system)

Run it by either copying the source code into `main.s`, or changing the ENTRYPOINT in the `makefile` to be `example` and rebuilding.
