cmake_minimum_required(VERSION 3.6)
project(DebugSolThreads)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES1
        cpp_thread_00.cpp
        cpp_thread_01.cpp
        cpp_thread_02.cpp)
set(SOURCE_FILES2
        posix_thread_00.cpp
        posix_thread_01.cpp
        posix_thread_02.cpp)

add_subdirectory(image_processing)
add_subdirectory(part_2)
add_subdirectory(part_3)

add_executable(CppThreads ${SOURCE_FILES1})
add_executable(PosixThreads ${SOURCE_FILES2})
