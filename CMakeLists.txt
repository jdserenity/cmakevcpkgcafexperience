cmake_minimum_required(VERSION 3.10)

set(CMAKE_TOOLCHAIN_FILE "${CMAKE_CURRENT_SOURCE_DIR}/config/vcpkg/scripts/buildsystems/vcpkg.cmake"
  CACHE STRING "Vcpkg toolchain file")
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

project(cmake-vcpkg-exp)

find_package(fmt REQUIRED)
find_package(caf REQUIRED)

add_executable(cmake-vcpkg-exp src/main.cpp)

target_link_libraries(cmake-vcpkg-exp PRIVATE fmt::fmt CAF::io CAF::core)