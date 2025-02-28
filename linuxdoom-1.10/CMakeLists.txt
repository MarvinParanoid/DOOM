cmake_minimum_required(VERSION 3.31)
project(doom)

set(CMAKE_C_STANDARD 17)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_HOME_DIRECTORY}/bin)

add_compile_options(-g -o2 -Wall -m32 -DNORMALUNIX -DLINUX)
add_link_options(-lX11 -lXext -lm -m32)

set(ASAN true)
if (${ASAN})
    add_compile_options(-fsanitize=address)
    add_link_options(-fsanitize=address)
endif ()

file(GLOB SOURCES ./*.c)
add_executable(doom ${SOURCES})
