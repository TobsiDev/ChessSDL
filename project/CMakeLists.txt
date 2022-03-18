cmake_minimum_required(VERSION 3.0.0)
project(AudioWiz VERSION 0.1.0)

include(CTest)
enable_testing()

add_subdirectory(src) # Adds a subfolder here

# If you have to include lib's via vcpkg
# you can add them here
find_package(SDL2 REQUIRED)
include_directories(SDL2Test ${SDL2_INCLUDE_DIRS})

add_executable(AudioWiz main.cpp)
target_link_libraries(AudioWiz PRIVATE src SDL2 SDL2main SDL2_ttf imgui)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)