cmake_minimum_required(VERSION 4.0)
project(mustache)
add_library(mustache INTERFACE)

option(MUSTACHE_BUILD_TESTS Off)

target_compile_features(mustache INTERFACE cxx_std_17)
target_sources(mustache INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/mustache.hpp)
target_include_directories(mustache INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})

if(MUSTACHE_BUILD_TESTS)
    add_subdirectory(tests)
endif()
