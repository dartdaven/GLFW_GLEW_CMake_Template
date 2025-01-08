# GLFW_GLEW_CMake_Template

## Overview
This repository provides a template for setting up a project using GLFW, GLEW, and CMake. It serves as a starting point for developing OpenGL applications.
This project is meant to be multiplatform and compile on windows, linux and mac.
Dependencies are downloaded during the CMake stage of creating build files, you can change the preferred version of deps in external/CMakeLists.txt.

## Features
- GLFW for creating windows and handling input
- GLEW for managing OpenGL extensions
- CMake for project configuration and build management

## Getting Started

### Clone the Repository
```sh
git clone https://github.com/dartdaven/GLFW_GLEW_CMake_Template.git
cd GLFW_GLEW_CMake_Template
```

### Build the Project
```sh
cmake -B build
cmake --build build
```