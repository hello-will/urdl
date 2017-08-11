cmake_minimum_required(VERSION 3.5)
project(example CXX)

set(LIBS
    urdl_static
    boost_system
    boost_thread
    boost_coroutine
    boost_unit_test_framework
    pthread
    crypto
    ssl)

add_executable(
    get1
    ${CMAKE_CURRENT_LIST_DIR}/get1.cpp
)
target_link_libraries(
    get1
    ${LIBS}
)

add_executable(
    get2
    ${CMAKE_CURRENT_LIST_DIR}/get2.cpp
)
target_link_libraries(
    get2
    ${LIBS}
)

add_executable(
    multiget1
    ${CMAKE_CURRENT_LIST_DIR}/multiget1.cpp
)
target_link_libraries(
    multiget1
    ${LIBS}
)

add_executable(
    multiget2
    ${CMAKE_CURRENT_LIST_DIR}/multiget2.cpp
)
target_link_libraries(
    multiget2
    ${LIBS}
)
