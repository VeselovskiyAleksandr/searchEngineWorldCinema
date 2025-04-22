cmake_minimum_required (VERSION 3.8)
project (serverTests)
include(FetchContent)
FetchContent_Declare( googletest
URL
https://github.com/google/googletest/archive/609281088cfefc76f9d0ce8 2e1ff6c30cc3591e5.zip )
FetchContent_MakeAvailable(googletest)
enable_testing()
add_executable (serverTests serverTests.cpp)
target_include_directories(${gtest_SOURCE_DIR}/include ${INCLUDE_DIR})
target_link_libraries(searchEngineWorldCinema PRIVATE gtest_main)