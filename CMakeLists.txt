cmake_minimum_required(VERSION 3.19)

set(CMAKE_C_COMPILER "gcc")
set(CMAKE_CXX_COMPILER "g++")
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
    
project(learn-modern-cpp-kafka)

include_directories(/usr/local/include)
include_directories(${PROJECT_SOURCE_DIR}/third_party/modern-cpp-kafka/include)

add_subdirectory(src)
