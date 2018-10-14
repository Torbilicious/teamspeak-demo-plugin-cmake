cmake_minimum_required(VERSION 3.12)
project(teamspeak-demo-plugin)

set(CMAKE_CXX_STANDARD 14)

set(dir ${CMAKE_CURRENT_SOURCE_DIR})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${dir}/lib")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${dir}/lib")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${dir}/bin")


list(APPEND SOURCES plugin.cpp
        plugin.h
        include/teamlog/logtypes.h
        include/teamspeak/clientlib_publicdefinitions.h
        include/teamspeak/public_definitions.h
        include/teamspeak/public_errors.h
        include/teamspeak/public_errors_rare.h
        include/teamspeak/public_rare_definitions.h
        include/plugin_definitions.h
        include/ts3_functions.h)


add_library(teamspeak-demo-plugin SHARED ${SOURCES})
#add_executable(teamspeak-demo-plugin ${SOURCES})
