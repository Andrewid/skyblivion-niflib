cmake_minimum_required(VERSION 2.8)
project(mikktspace)
set(PROJECT_VERSION_MAJOR "0")
set(PROJECT_VERSION_MINOR "1")
set(PROJECT_VERSION_PATCH "0")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -std=c1x")
set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS} ${CMAKE_C_FLAGS_DEBUG} -ggdb -DDEBUG")
set(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS} ${CMAKE_C_FLAGS_RELEASE} -O2")
set(SOURCES mikktspace.h mikktspace.c)
add_library(mikktspace STATIC ${SOURCES})
install(TARGETS mikktspace ARCHIVE DESTINATION ".")
