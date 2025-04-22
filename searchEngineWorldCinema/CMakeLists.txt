# CMakeList.txt: проект CMake для searchEngineWorldCinema; включите исходный код и определения,
# укажите здесь логику для конкретного проекта.
#
cmake_minimum_required (VERSION 3.8)
#project ("searchEngineWorldCinema")
#include(FetchContent)
#FetchContent_Declare( googletest
#URL
#https://github.com/google/googletest/archive/609281088cfefc76f9d0ce8 2e1ff6c30cc3591e5.zip )
FetchContent_MakeAvailable(googletest)
#enable_testing()
# Добавьте источник в исполняемый файл этого проекта.
add_executable (searchEngineWorldCinema   "include/Configuration.h" "include/ConverterJSON.h" "include/Entry.h"   "src/ConverterJSON.cpp" "src/searchEngineWorldCinema.cpp")
# TODO: Добавьте тесты и целевые объекты, если это необходимо.
target_link_libraries(searchEngineWorldCinema PRIVATE nlohmann_json::nlohmann_json)
#target_link_libraries(searchEngineWorldCinema PRIVATE gtest_main)
#include(GoogleTest)
#gtest_discover_tests(searchEngineWorldCinema )
target_include_directories(searchEngineWorldCinema PUBLIC include)