
cmake_minimum_required(VERSION 3.10)
project(DynamicArrayProject C)

# Use C instead of C++
set(CMAKE_C_STANDARD 11)

# Set output directory for executable
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# Include directories
include_directories(include lib src)

# Gather all .c files in src and lib
file(GLOB_RECURSE MAIN_SRC
    "src/*.c"
    "lib/*.c"
)

# Create the executable
add_executable(main ${MAIN_SRC})

