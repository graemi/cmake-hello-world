cmake_minimum_required (VERSION 3.8)
project (CMakeHelloWorld)

#version number
set (CMakeHelloWorld_VERSION_MAJOR 1)
set (CMakeHelloWorld_VERSION_MINOR 1)

set (CMAKE_CXX_STANDARD 14)

#include the subdirectory containing our libs
add_subdirectory (hello)
include_directories(hello)
#indicate the entry point for the executable
add_executable (hello-world hello hello_world.cpp)

# Indicate which libraries to include during the link process.
target_link_libraries (hello-world hello)

install (TARGETS hello-world DESTINATION bin)
