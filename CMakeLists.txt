cmake_minimum_required(VERSION 3.14) # Don't know why this version
Project(OpenGL)

set(EXECUTABLE_NAME ${PROJECT_NAME})

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_BUILD_TYPE Debug) # Change to Release when needed

# Set path to another CMakeLists.txt with external dependencies
add_subdirectory(external)

file(GLOB_RECURSE SOURCES source/*.cpp)

add_executable(${EXECUTABLE_NAME} ${SOURCES})
target_link_libraries(${EXECUTABLE_NAME} glfw libglew_static glm)