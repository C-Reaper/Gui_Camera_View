# Project README

## Overview
The project is a simple application that captures video from a camera and displays it in a window using a custom library. The application supports building on multiple platforms including Linux, Windows, Wine, and WebAssembly.

## Features
- Video capture using RLCamera_New
- Display of captured video frames in a window
- Basic window management functions (Setup, Update, Delete)

## Project Structure
### Prerequisites
- C/C++ Compiler and Debugger (GCC for Linux and Windows)
- Make utility
- Standard development tools
- Libraries needed:
  - For Linux: `libX11`, `libpng`, `libjpeg`
  - For Wine: `user32`, `gdi32`, `winmm`
  - For WebAssembly: `emcc`

## Build & Run
### Building
The project supports building on multiple platforms using different Makefiles. Here are the steps for each platform:

#### Linux
To build and run on Linux:
```sh
make -f Makefile.linux all
make -f Makefile.linux exe
```

#### Windows
To build and run on Windows (assuming a Unix-like shell):
```sh
make -f Makefile.windows all
make -f Makefile.windows exe
```

#### Wine
To cross-compile for Windows using Wine:
```sh
make -f Makefile.wine all
make -f Makefile.wine exe
```

#### WebAssembly (Emscripten)
To build and run the project in a web browser:
```sh
make -f Makefile.web all
make -f Makefile.web exe
```

### Running
The built executable can be run directly after building. For example, on Linux:
```sh
./build/Main
```
On Windows, you might need to use Wine to run the .exe file if not natively supported.

This README provides a basic overview of the project structure and build process for different platforms.