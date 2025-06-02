cmake_minimum_required(VERSION 3.8)
set(NAME "nukem_detours")

project(${NAME})

add_library(${NAME} STATIC
   ${CMAKE_CURRENT_SOURCE_DIR}/detours/Detours.h
   ${CMAKE_CURRENT_SOURCE_DIR}/detours/Detours.cpp
   ${CMAKE_CURRENT_SOURCE_DIR}/detours/Detours32.cpp
   ${CMAKE_CURRENT_SOURCE_DIR}/detours/Detours64.cpp
   ${CMAKE_CURRENT_SOURCE_DIR}/detours/stdafx.h
   ${CMAKE_CURRENT_SOURCE_DIR}/detours/stdafx.cpp
   ${CMAKE_CURRENT_SOURCE_DIR}/detours/HideStaticLibSymbols.c
)

target_link_libraries(
	${NAME}
	PRIVATE
	
)

target_include_directories(${NAME} PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/detours
)