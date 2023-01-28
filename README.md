# CS639S23_Demos

Software artifacts and Demos for CS639 (Spring 2023) "Parallel and Throughput-Optimized Programming"

# Build with CMake

Current CMake config will generate 2 versions for all the build targets: one with OpenMP enabled and one with OpenMP disabled.

## MacOS

1. Install `llvm` and `libomp` with brew.
2. If llvm clang compiler and libraries are not installed in `/usr/local/opt/llvm/bin/clang++` and `/usr/local/opt/llvm/lib`, change location in `CMakeLists.txt`.
3. Generate project with `cmake -S . -B build/`, `build/` directory is ignored by `.gitignore`.
4. Build with `make -C build/`
5. All the binaries build targets are in `build/bin` directory.

## Linux (Varified on UW-Madison CS Lab)

1. Generate project with `cmake -S . -B build/`, `build/` directory is ignored by `.gitignore`.
2. Build with `make -C build/`
3. All the binaries build targets are in `build/bin` directory.
