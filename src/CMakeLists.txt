cmake_minimum_required(VERSION 3.31)
project(doom)

set(CMAKE_C_STANDARD 17)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_HOME_DIRECTORY}/bin)

add_compile_options(-g -o2 -Wall -DNORMALUNIX -DLINUX -DSDL)
add_link_options(-lm -lSDL)

if (${ASAN})
    add_compile_options(-fsanitize=address)
    add_link_options(-fsanitize=address)
endif ()

file(GLOB SOURCES ./*.c)
add_executable(doom ${SOURCES})
