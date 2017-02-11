# chip8swemu

chip8swemu is a multiplatform CHIP-8 emulator/interpreter written in C.

## Features

* Cross-platform support through [SDL2](http://libsdl.org): tested on Windows, but should work on Linux and macOS with minor or no changes.
* Uses [imgui](https://github.com/ocornut/imgui) for the user interface.
* Native file selection dialog on Windows.
* Configurable instructions per second rate (840 by default).
* Configurable color palette.
* Configuration stored in a config.ini file.

The emulator core (`chip8.h`, `chip8.c`) depends only on standard C99 libraries so it can be easily reusable in other projects. The [chip8duino](https://github.com/AlfonsoJLuna/chip8duino) game console uses it as a library.

## Screenshots

![breakout](/screenshots/breakout.png)

![tetris](/screenshots/tetris.png)

![invaders](/screenshots/invaders.png)

## Documentation

- [CHIP-8 article on Wikipedia](https://en.wikipedia.org/wiki/CHIP-8)
- [Cowgod's CHIP-8 Technical Reference](http://devernay.free.fr/hacks/chip8/C8TECH10.HTM)
- [How to write an emulator (CHIP-8 interpreter)](http://www.multigesture.net/articles/how-to-write-an-emulator-chip-8-interpreter/)
- [Complete collection of all known CHIP-8 games](http://www.chip8.com/?page=109): Some of these programs are included in the release for testing the emulator. Those programs are public domain or freely distributed by their respective authors.

## Dependencies

chip8swemu uses the following libraries:
- [SDL 2.0.5](http://libsdl.org)
- [imgui 1.49](https://github.com/ocornut/imgui)

## Building on Windows

1. [Download](http://tdm-gcc.tdragon.net/download) and install the TDM-GCC compiler suite. Be sure you check `Add to PATH` during instalation.
2. Clone or download this repository
3. [Download](https://www.libsdl.org/download-2.0.php) SDL 2.0.5 development libraries for MinGW and extract them to `chip8swemu/libraries/SDL2-2.0.5/...`
4. [Download](https://github.com/ocornut/imgui/releases) imgui 1.49 source code and place it in `chip8swemu/libraries/imgui-1.49/`
6. Open a command prompt and type: `mingw32-make`
