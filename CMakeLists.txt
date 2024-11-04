cmake_minimum_required(VERSION 3.25)
project(PanguLU LANGUAGES C CXX CUDA)
cmake_policy(SET CMP0146 OLD)

find_package(CUDAToolkit REQUIRED)
find_package(BLAS REQUIRED)
find_package(MPI REQUIRED)
find_package(OpenMP REQUIRED)

add_subdirectory(src)

target_include_directories(pangulu PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_link_libraries(pangulu PRIVATE metis CUDA::cudart BLAS::BLAS MPI::MPI_C OpenMP::OpenMP_C)
target_compile_definitions(pangulu PUBLIC -DGPU_OPEN -DCALCULATE_TYPE_R64 -DMETIS)
set_target_properties(pangulu PROPERTIES CUDA_ARCHITECTURES "70;80;86;90a")

add_subdirectory(examples)
