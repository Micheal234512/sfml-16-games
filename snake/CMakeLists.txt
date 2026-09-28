cmake_minimum_required(VERSION 3.16)
project(snake LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(BUILD_SHARED_LIBS OFF)

include(FetchContent)
FetchContent_Declare(SFML
    GIT_REPOSITORY https://github.com/SFML/SFML.git
    GIT_TAG 2.6.1
    GIT_SHALLOW ON)
FetchContent_MakeAvailable(SFML)

add_executable(snake main.cpp)
target_link_libraries(snake PRIVATE sfml-graphics)