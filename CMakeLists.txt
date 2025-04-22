# CMakeList.txt: файл проекта CMake верхнего уровня; проведите глобальную конфигурацию
# и включите сюда подпроекты.
#
cmake_minimum_required (VERSION 3.8)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
project ("searchEngineWorldCinema")
include(FetchContent)
#FetchContent_Declare( googletest
#URL
#https://github.com/google/googletest/archive/609281088cfefc76f9d0ce8 2e1ff6c30cc3591e5.zip )
#ADD_SUBDIRECTORY (gtest-1.6.0)###
#FetchContent_MakeAvailable(googletest)
#enable_testing()
#include_directories(${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})
#set(gtest_disable_pthreads on)
#set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
#include(GoogleTest)

#target_link_libraries(searchEngineWorldCinema PRIVATE gtest_main)

#gtest_discover_tests(search_engine)
#gtest_discover_tests(searchEngineWorldCinema)



# Включите подпроекты.
add_subdirectory ("searchEngineWorldCinema")
add_subdirectory(nlohmann.json)
add_subdirectory(tests)