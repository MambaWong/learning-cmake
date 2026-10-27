cmake_minimum_required(VERSION 3.10)

project(hello-world LANGUAGES C)

message(STATUS "This is BINARY dir " ${PROJECT_BINARY_DIR})
message(STATUS "This is SOURCE dir " ${PROJECT_SOURCE_DIR})

add_executable(hello-world main.c)
