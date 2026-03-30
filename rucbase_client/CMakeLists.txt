cmake_minimum_required(VERSION 3.16)
project(rucbase_client)

set(CMAKE_CXX_STANDARD 20)
find_package(Threads REQUIRED)

set(CMAKE_CXX_FLAGS "-Wall -O0 -g -ggdb3")
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -O0 -g")
set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -O0 -g")


add_executable(${PROJECT_NAME} main.cpp)


target_link_libraries(rucbase_client
        pthread readline 
)