project(rpg_common_ros)
cmake_minimum_required(VERSION 2.8.3)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

add_definitions(-std=c++11)

FILE(GLOB_RECURSE HEADERS "include/*")

list(APPEND SOURCES
  src/publish.cpp
  src/tf.cpp)

cs_add_library(${PROJECT_NAME} ${SOURCES} ${HEADERS})

cs_install()
cs_export()
