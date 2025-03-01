cmake_minimum_required(VERSION 3.31)
project(sndserver)

set(CMAKE_C_STANDARD 17)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_HOME_DIRECTORY}/bin)

add_compile_options(-g -o2)
add_link_options(-lm)

if (NOT ${X86_64})
    add_compile_options(-m32)
    add_link_options(-m32)
endif ()

file(GLOB SOURCES ./*.c)
add_executable(sndserver ${SOURCES})
