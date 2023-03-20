cmake_minimum_required(VERSION 3.24)
project(module4assignment)

set(CMAKE_CXX_STANDARD 17)

#Add the google test subdirectory
add_subdirectory(googletest)

#include googletest/include dir
include_directories(googletest/include)

#include the googlemock/include dir
include_directories(googlemock/include)

add_executable(module4assignment test.cpp)

#Link with GoogleTest
target_link_libraries(module4assignment gtest gtest_main)

#Link with GoogleMock
target_link_libraries(module4assignment gmock gmock_main)

