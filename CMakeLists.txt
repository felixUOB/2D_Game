cmake_minimum_required(VERSION 3.15)
project(2D_Game)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add GLFW include path
include_directories(
    $ENV{HOME}/Dev/glfw-3.4/include
    /Users/felix/Dev/glad/include
)

# Add GLFW static library path
link_directories("$ENV{HOME}/Dev/glfw-3.4/build/src")

# Add executable
add_executable(
    2D_Game main.cpp
    /Users/felix/Dev/glad/src/glad.c

)

# Link GLFW and macOS frameworks
target_link_libraries(2D_Game
    glfw3
    "-framework Cocoa"
    "-framework OpenGL"
    "-framework IOKit"
    "-framework CoreVideo"
)
