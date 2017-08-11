cmake_minimum_required(VERSION 3.0)
project(urdl CXX)

find_package(Boost)
find_package(OpenSSL)
option(URDL_HEADER_ONLY "urdl header only" OFF)
option(URDL_TEST "compile urdl test" OFF)
option(URDL_EXAMPLE "compile urdl example" OFF)

include_directories(
    ${Boost_INCLUDE_DIRS}
    ${OpenSSL_INCLUDE_DIRS}
    ${CMAKE_CURRENT_LIST_DIR}/include
)
link_directories(
    ${Boost_LIBRARY_DIRS}
    ${OpenSSL_LIBRARY_DIRS}
)

if (CMAKE_COMPILER_IS_GNUCXX)
add_compile_options(
    -pipe
    -Wall
    -Wextra
    -fPIC
)
endif(CMAKE_COMPILER_IS_GNUCXX)

if(NOT URDL_HEADER_ONLY)
    add_subdirectory(src)
endif()

if(URDL_TEST)
    add_subdirectory(test)
endif()

if(URDL_EXAMPLE)
    add_subdirectory(example)
endif()
