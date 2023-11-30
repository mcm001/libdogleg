cmake_minimum_required(VERSION 3.23)

project(dogleg)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 20)

add_library(
    dogleg 
    dogleg.cpp
)

target_include_directories(dogleg PRIVATE 
    ../suitesparse/CHOLMOD/Include
    ../suitesparse/SuiteSparse_config
)
