cmake_minimum_required(VERSION 3.20)
project(Hazel)

find_package(spdlog REQUIRED)

add_library(compiler_flags INTERFACE)
target_compile_features(compiler_flags INTERFACE cxx_std_20)

add_subdirectory(Hazel)
add_subdirectory(Sandbox)