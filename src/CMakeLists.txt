cmake_minimum_required(VERSION 3.16)

set(CMAKE_C_STANDARD 99)
project(src VERSION 1)
message("-- CMAKE_PROJECT_VERSION = ${CMAKE_PROJECT_VERSION}")
add_executable(PassMann main.c database.c encryption.c log.c input.c RawMode.c)
include_directories(${CMAKE_SOURCE_DIR})
set(CMAKE_BUILD_TYPE Debug)

target_link_libraries(PassMann PUBLIC c)
target_link_libraries(PassMann PUBLIC m)
target_link_libraries(PassMann PUBLIC sodium)
