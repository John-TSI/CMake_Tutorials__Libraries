cmake_minimum_required(VERSION 3.12)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(Libraries VERSION 1.0.0)


add_library(say_hello src/hello.hpp src/hello.cpp)

add_executable(${PROJECT_NAME} src/main.cpp)


target_link_libraries(${PROJECT_NAME} PRIVATE say_hello)
