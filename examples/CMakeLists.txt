add_executable(example example.c)
target_link_libraries(example PUBLIC pangulu MPI::MPI_C m)
