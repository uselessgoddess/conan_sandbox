cmake_minimum_required(VERSION 3.19)
project(conan_sandbox)
set(CONAN_DISABLE_CHECK_COMPILER TRUE) ## like it
include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

add_executable(conan_sandbox main.cpp)
set_target_properties(conan_sandbox PROPERTIES CXX_STANDARD 20)

target_link_libraries(conan_sandbox PRIVATE CONAN_PKG::gtest)
