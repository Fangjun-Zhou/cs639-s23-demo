# -------------- LaplacianStencil Build Targets -------------- #

# TODO: Build all targets.

file(
    GLOB
    LAPLACIAN_SRC
    ${CMAKE_CURRENT_SOURCE_DIR}/LaplacianStencil_0_0/*.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/LaplacianStencil_0_0/*.h
)
# OpenMP disabled.
add_executable(laplacian ${LAPLACIAN_SRC})
# OpenMP enabled.
add_executable(laplacian-omp ${LAPLACIAN_SRC})
target_link_libraries(laplacian-omp PRIVATE -fopenmp)
target_compile_options(laplacian-omp PRIVATE -fopenmp)