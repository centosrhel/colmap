cmake_minimum_required(VERSION 2.8.11)

project(TestProject)

find_package(COLMAP REQUIRED)
# or to require a specific version: find_package(COLMAP 3.4 REQUIRED)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include_directories(${COLMAP_INCLUDE_DIRS})
link_directories(${COLMAP_LINK_DIRS})

add_executable(hello_world hello_world.cc)
target_link_libraries(hello_world ${COLMAP_LIBRARIES})
