cmake_minimum_required(VERSION 3.10)
project(ConfigurationManager)

find_package(sdbus-c++ REQUIRED)

add_executable(ConfigurationManager
    src/main.cpp
    src/ApplicationConfig.cpp
    src/ApplicationConfiguration.cpp
)

target_link_libraries(ConfigurationManager PRIVATE sdbus-c++ nlohmann_json::nlohmann_json)
target_include_directories(ConfigurationManager PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src)