cmake_minimum_required(VERSION 3.10)

project(glad VERSION 4.3)
add_library(glad STATIC src/glad.c)
target_include_directories(glad PUBLIC include)