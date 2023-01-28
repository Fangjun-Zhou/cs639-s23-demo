cmake_minimum_required(VERSION 3.22.1)

project(CS639S23)

# ------------------- Environment Settings ------------------- #

if (APPLE)
    # Need llvm installed.
    set(CMAKE_CXX_COMPILER /usr/local/opt/llvm/bin/clang++)
    # Link llvm libraries.
    link_directories(/usr/local/opt/llvm/lib)
elseif(UNIX AND NOT APPLE)
    # Use g++ on Linux.
    set(CMAKE_CXX_COMPILER g++)
else()
    # TODO: Add Windows and Linux support.
    message("Platform not support.")
endif()

# -------------------------- Options ------------------------- #

# Binary build path.
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# ----------------------- Build Targets ---------------------- #
add_subdirectory(LaplacianStencil)