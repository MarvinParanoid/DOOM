### Description
Just another vanilla fork of Doom.

### Building

```
cmake -DCMAKE_BUILD_TYPE=Debug -B /home/rofl/DOOM/cmake-build-debug
cmake --build /home/rofl/DOOM/cmake-build-debug --target doom sndserver -j 8
```

### How to run

Requirements: 
- Xephyr for emulation 8bit display
- (optionally) - emulator of the /dev/dsp device (on Arch I've found ossp in AUR repo)
```
# create a screen
Xephyr :2 -ac -screen 640x400x8 

# run Doom
export DOOMWADDIR=<path_to_wad_dir>
DISPLAY=:2
bin/doom -2
```