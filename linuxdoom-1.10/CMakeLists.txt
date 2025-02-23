cmake_minimum_required(VERSION 3.31)
project(doom)

set(CMAKE_C_STANDARD 17)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_HOME_DIRECTORY}/bin)

add_compile_options(-Wall -m32 -DNORMALUNIX -DLINUX -Wno-error=implicit-int)
add_link_options(-lX11 -lXext -lm -m32)

file(GLOB SOURCES ./*.c)
add_executable(doom ${SOURCES})
