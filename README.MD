### Description
Just another vanilla fork of Doom to run it on modern systems.

#### Done:
- build on x86_64 linux
- CMake instead of make
- SDL for graphics 
- sounds (with emulating of /dev/dsp device)

#### To be done:
- fix 64bit related bugs (can be reproduced with sanitizer)
- SDL for sounds
- music
- move to SDL2
- port on Nintendo Switch

### Building

Requirements:
- gcc/clang
- SDL library

```
cmake -DCMAKE_BUILD_TYPE=Debug -B /home/rofl/DOOM/cmake-build-debug
cmake --build /home/rofl/DOOM/cmake-build-debug --target doom sndserver -j 8
```

### How to run

Optionally: for sounds emulator of the /dev/dsp device is needed (on Arch I've found ossp in AUR repo)

```
export DOOMWADDIR=<path_to_wad_dir>
bin/doom
```