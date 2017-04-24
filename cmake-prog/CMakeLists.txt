cmake_minimum_required(VERSION 3.7)
project(cmake-prog)
cmake_policy(SET CMP0022 NEW)

set(CMAKE_CXX_STANDARD 11)

if (NOT TARGET cmake_lib)
    find_package(cmakeLib)
endif()

set(SOURCE_FILES main.cpp)
add_executable(cmake_prog ${SOURCE_FILES})
target_link_libraries(cmake_prog cmake_lib cmake_lib3)
