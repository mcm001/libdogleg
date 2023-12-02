cmake_minimum_required(VERSION 3.20)

project(dogleg)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 20)

add_library(
    dogleg 
    dogleg.cpp
)

target_include_directories(dogleg PRIVATE 
    /usr/include/suitesparse
    # ../suitesparse-windows-binaries/CHOLMOD/Include
    # ../suitesparse-windows-binaries/SuiteSparse_config/include
)

target_link_libraries(dogleg PUBLIC 
    suitesparseconfig cholmod lapack
)

