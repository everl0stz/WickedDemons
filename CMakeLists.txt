cmake_minimum_required(VERSION 3.17)
project(WickedDemons)

set(CMAKE_CXX_STANDARD 17)

add_executable(WickedDemons
  src/main.cpp
)

set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "Build the GLFW example programs" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "Build the GLFW test programs" FORCE)
set(GLFW_INSTALL OFF "Generate installation target" FORCE)
set(BUILD_EXAMPLES OFF CACHE BOOL "Build example apps" FORCE)

add_subdirectory(deps/glfw)
include_directories(deps/glad/include)
include_directories(deps/glfw/include)