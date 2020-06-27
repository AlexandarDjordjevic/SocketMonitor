cmake_minimum_required(VERSION 3.8)

set(this SocketMonitor)

project(${this})

set(CMAKE_CXX_STANDARD 11)

set(Src 
    src/SocketMonitor.cpp
)

set(Include 
    include/SocketMonitor.hpp
)

add_library(${this} STATIC ${Src} ${Include})

set_target_properties(${this} PROPERTIES
    FOLDER Libraries
)

target_include_directories(${this} PUBLIC include)

target_link_libraries(${this} PUBLIC Socket)
