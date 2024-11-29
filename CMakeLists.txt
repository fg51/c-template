# cmake version
cmake_minimum_required(VERSION 3.21)

# project info
project(mypro
  VERSION 1.0
  DESCRIPTION "myproj project"
  LANGUAGES C
)

# in-source build-guard
if(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_BINARY_DIR})
  message(FATAL_ERROR "In-source builds not allowed. Please make a new directory (called a build directory) and run CMake from ther. You may need to remove CMakeCache.txt. ")
endif()

# read CMakeLists.txt in sub-directory.
add_subdirectory(src/lib)
add_subdirectory(src/bin)

target_compile_options(myapp PRIVATE -Wall -Wextra)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_COMPILER clang)
