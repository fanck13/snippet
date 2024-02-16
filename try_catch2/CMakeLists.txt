cmake_minimum_required(VERSION 3.21)
project(try_catch2)

add_executable(${PROJECT_NAME} main.cpp)

find_package(Catch2 CONFIG REQUIRED)
target_link_libraries(${PROJECT_NAME} PRIVATE Catch2::Catch2 Catch2::Catch2WithMain)