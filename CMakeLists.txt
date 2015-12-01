project(Interpo-Apps)
cmake_minimum_required (VERSION 2.8)

find_package(Eigen3 REQUIRED)
include_directories(${EIGEN3_INCLUDE_DIR})

set (ROOT ${CMAKE_CURRENT_SOURCE_DIR})
set (SRC  ${ROOT}/main.cpp )

list( APPEND CMAKE_CXX_FLAGS "-std=c++11 -fPIC -Wall -Wpedantic -Wextra")

add_executable (bezier ${SRC})
