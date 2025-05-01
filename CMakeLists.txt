cmake_minimum_required(VERSION 3.0)
project(lua)

file(GLOB LUA_SRC
    ${CMAKE_CURRENT_SOURCE_DIR}/*.c
)

list(REMOVE_ITEM LUA_SRC "${CMAKE_CURRENT_SOURCE_DIR}/luac.c")

add_library(lua STATIC ${LUA_SRC})
target_include_directories(lua PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
