cmake_minimum_required(VERSION 3.31)
project(all)

set(X86_64 true)
set(ASAN false)
set(SDL true)

add_subdirectory(linuxdoom-1.10)
add_subdirectory(sndserv)