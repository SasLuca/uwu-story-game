cmake_minimum_required(VERSION 3.0)
project(uwu-story-game C)

set(CMAKE_C_STANDARD 99)

# Setting parameters for raylib
set(BUILD_EXAMPLES OFF CACHE BOOL "" FORCE) # don't build the supplied examples
set(BUILD_GAMES    OFF CACHE BOOL "" FORCE) # or games

add_subdirectory(libs/raylib)
include_directories(libs/)

add_executable(uwu-story-game src/main.c libs/libco.c)
target_link_libraries(uwu-story-game PRIVATE raylib)