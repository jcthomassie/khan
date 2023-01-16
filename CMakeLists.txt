cmake_minimum_required(VERSION 3.0.0)
project(khan)

set(SOURCES
	src/main.cpp
)

add_subdirectory(libs/socket.io-client-cpp)
include_directories(libs/socket.io-client-cpp/src)

add_executable(khan ${SOURCES})

target_link_libraries(khan sioclient)