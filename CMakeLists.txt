cmake_minimum_required(VERSION 3.22)
project(homework1)

enable_language(CXX)

set (TARGET hw1)
#set(CMAKE_BUILD_NUMBER 3)
set(BUILD_NUMBER TRUE)

configure_file(config.hpp.in config.hpp)

add_executable(${TARGET} 
    main.cpp
)
target_include_directories(${TARGET} PRIVATE
    ${CMAKE_CURRENT_BINARY_DIR}
)

message("hello ${CMAKE_BUILD_NUMBER}")