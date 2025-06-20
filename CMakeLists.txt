cmake_minimum_required(VERSION 3.10)
project(DBusConfigurationManager LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_program(CLANG_FORMAT "clang-format")
if(CLANG_FORMAT)
    add_custom_target(format
        COMMAND ${CLANG_FORMAT} -i $<TARGET_PROPERTY:format_sources,SOURCES>
        COMMENT "Formatting source code..."
    )
endif()

add_subdirectory(src/ConfigurationManager)
add_subdirectory(src/comManageApplication1)