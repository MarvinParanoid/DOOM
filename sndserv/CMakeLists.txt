cmake_minimum_required(VERSION 3.31)
project(sndserver)

set(CMAKE_C_STANDARD 17)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_HOME_DIRECTORY}/bin)

add_link_options(-lm)

file(GLOB SOURCES ./*.c)
add_executable(sndserver ${SOURCES})
