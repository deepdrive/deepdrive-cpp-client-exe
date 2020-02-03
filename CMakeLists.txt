cmake_minimum_required(VERSION 3.15)
project(deepdrive_cpp_client_exe)

set(CMAKE_CXX_STANDARD 14)

add_library(deepdrive_cpp_client SHARED IMPORTED)
set_target_properties(deepdrive_cpp_client PROPERTIES
  IMPORTED_LOCATION "/home/c2/src/deepdrive-cpp-client/cmake-build-debug/libdeepdrive_cpp_client.so"
  INTERFACE_INCLUDE_DIRECTORIES "/home/c2/src/deepdrive-cpp-client"
)

add_executable(deepdrive_cpp_client_exe main.cpp)

target_link_libraries(deepdrive_cpp_client_exe deepdrive_cpp_client)