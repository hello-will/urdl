cmake_minimum_required(VERSION 3.0)
project(src CXX)

aux_source_directory(${CMAKE_CURRENT_LIST_DIR} SRC_LIST)

set(LIB_NAME urdl_static)
add_library(
    ${LIB_NAME}
    STATIC
    ${SRC_LIST}
)
