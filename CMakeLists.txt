cmake_minimum_required(VERSION 3.10)

set(CMAKE_TOOLCHAIN_FILE "${CMAKE_CURRENT_SOURCE_DIR}/vcpkg/scripts/buildsystems/vcpkg.cmake"
  CACHE STRING "Vcpkg toolchain file")
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

project(vcpkg2)

find_package(fmt REQUIRED)
find_package(caf REQUIRED)

add_executable(vcpkg2 src/main.cpp)

target_link_libraries(vcpkg2 PRIVATE fmt::fmt CAF::io CAF::core)