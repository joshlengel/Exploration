cmake_minimum_required(VERSION 3.0)

project(exploration VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_CXX_FLAGS "-Wall")

# build

set(ROOT ${CMAKE_CURRENT_SOURCE_DIR})
set(SRC ${ROOT}/src)
set(INCLUDE ${ROOT}/include)
set(BIN ${ROOT}/bin)

file(GLOB_RECURSE sources "${SRC}/*.cpp")

set(EXECUTABLE_OUTPUT_PATH ${BIN})

add_executable(exploration ${sources})
target_include_directories(exploration PRIVATE ${INCLUDE})