### Description
Just another vanilla fork of Doom to run it on modern systems.

#### Done:
- build on x86_64 linux
- CMake instead of make
- SDL for graphics and sounds

#### To be done:
- fix 64bit related bugs (can be reproduced with sanitizer)
- music
- move to SDL2
- port on Windows
- port on Nintendo Switch and DS

### Building

Requirements:
- gcc/clang
- SDL library

```
cd DOOM 
mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Debug ..
cmake --build . -j 8
```

### How to run

```
export DOOMWADDIR=<path_to_wad_dir>
bin/doom
```