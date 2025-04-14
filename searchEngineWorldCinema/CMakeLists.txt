# CMakeList.txt: проект CMake для searchEngineWorldCinema; включите исходный код и определения,
# укажите здесь логику для конкретного проекта.
#
cmake_minimum_required (VERSION 3.8)

# Добавьте источник в исполняемый файл этого проекта.
add_executable (searchEngineWorldCinema   "include/Configuration.h" "include/ConverterJSON.h" "include/Entry.h"   "src/ConverterJSON.cpp" "src/searchEngineWorldCinema.cpp")
# TODO: Добавьте тесты и целевые объекты, если это необходимо.
target_link_libraries(searchEngineWorldCinema PRIVATE nlohmann_json::nlohmann_json)
#target_link_libraries(searchEngineWorldCinema PRIVATE gtest_main)
#include(GoogleTest)
#gtest_discover_tests(searchEngineWorldCinema )
target_include_directories(searchEngineWorldCinema PUBLIC include)