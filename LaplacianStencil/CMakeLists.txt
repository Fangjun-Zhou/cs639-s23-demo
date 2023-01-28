# -------------- LaplacianStencil Build Targets -------------- #

file(
    GLOB
    LAPLACIAN_SRC
    ${CMAKE_CURRENT_SOURCE_DIR}/LaplacianStencil_0_0/*.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/LaplacianStencil_0_0/*.h
)
add_executable(laplacian ${LAPLACIAN_SRC})
add_executable(laplacian-omp ${LAPLACIAN_SRC})
target_link_libraries(laplacian-omp PRIVATE -fopenmp)
target_compile_options(laplacian-omp PRIVATE -fopenmp)