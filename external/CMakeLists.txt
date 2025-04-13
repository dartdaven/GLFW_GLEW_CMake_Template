set(EXTERNAL_DIR ${CMAKE_SOURCE_DIR}/external)
set(BUILD_SHARED_LIBS OFF CACHE BOOL "Build all libraries as static" FORCE)

include(FetchContent)

# ------ GLFW ------
FetchContent_Declare(
    GLFW
    GIT_REPOSITORY https://github.com/glfw/glfw.git
    GIT_TAG        3.3.8       # Specify the version you want to use
    SOURCE_DIR     ${EXTERNAL_DIR}/GLFW
)

set(GLFW_BUILD_EXAMPLES OFF)
set(GLFW_BUILD_TESTS OFF)
set(GLFW_BUILD_DOCS OFF)

FetchContent_MakeAvailable(GLFW)

# ------ GLEW ------
FetchContent_Declare(
    GLEW
    # This is a fork of the original GLEW repository that has CMake support
    GIT_REPOSITORY https://github.com/Perlmint/glew-cmake.git
    GIT_TAG        glew-cmake-2.2.0    # Specify the version you want to use
    SOURCE_DIR     ${EXTERNAL_DIR}/GLEW
)

add_definitions(-DGLEW_STATIC)

FetchContent_MakeAvailable(GLEW)

# ------ GLM ------
FetchContent_Declare(
    GLM
    GIT_REPOSITORY https://github.com/g-truc/glm.git
    GIT_TAG        1.0.1    # Specify the version you want to use
    SOURCE_DIR     ${EXTERNAL_DIR}/GLM
)

set(GLM_TEST_ENABLE OFF CACHE BOOL "Disable GLM unit tests")

FetchContent_MakeAvailable(GLM)