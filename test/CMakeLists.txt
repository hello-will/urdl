cmake_minimum_required(VERSION 3.5)
project(test CXX)

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
    istream
    ${CMAKE_CURRENT_LIST_DIR}/istream.cpp
)
target_link_libraries(
    istream
    ${LIBS}
)

add_executable(
    istreambuf
    ${CMAKE_CURRENT_LIST_DIR}/istreambuf.cpp
)
target_link_libraries(
    istreambuf
    ${LIBS}
)

add_executable(
    option_set
    ${CMAKE_CURRENT_LIST_DIR}/option_set.cpp
)
target_link_libraries(
    option_set
    ${LIBS}
)

add_executable(
    read_stream
    ${CMAKE_CURRENT_LIST_DIR}/read_stream.cpp
)
target_link_libraries(
    read_stream
    ${LIBS}
)

add_executable(
    url
    ${CMAKE_CURRENT_LIST_DIR}/url.cpp
)
target_link_libraries(
    url
    ${LIBS}
)
