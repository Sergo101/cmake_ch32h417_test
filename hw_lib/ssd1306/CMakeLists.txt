cmake_minimum_required(VERSION 3.20)

set(LIB_NAME lcd_oled)

file(GLOB sources
  ${CMAKE_CURRENT_LIST_DIR}/Src/*.c
  ${CMAKE_CURRENT_LIST_DIR}/Src/*.cpp
)

file(GLOB headers
  ${CMAKE_CURRENT_LIST_DIR}/Inc/*.*
  ${CMAKE_CURRENT_LIST_DIR}/Inc/Legacy/*.*
)

set(includes
  ${CMAKE_CURRENT_LIST_DIR}/Inc
  ${CMAKE_CURRENT_LIST_DIR}/Inc/Legacy
)

add_library(${LIB_NAME} INTERFACE)

target_sources(${LIB_NAME} INTERFACE ${sources} ${headers})
target_include_directories(${LIB_NAME} INTERFACE ${includes})

target_compile_definitions(${LIB_NAME} INTERFACE
)
