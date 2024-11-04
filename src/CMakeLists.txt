set(PANGULU_SRCS
        pangulu.c
        pangulu_gessm_fp64.c
        pangulu_kernel_interface.c
        pangulu_reorder.c
        pangulu_ssssm_fp64_cuda.c
        pangulu_tstrf_fp64_cuda.c
        pangulu_check.c
        pangulu_gessm_fp64_cuda.c
        pangulu_malloc.c
        pangulu_spmv_fp64.c
        pangulu_symbolic.c
        pangulu_utils.c
        pangulu_common.h
        pangulu_getrf_fp64.c
        pangulu_mpi.c
        pangulu_sptrsv.c
        pangulu_thread.c
        pangulu_addmatrix.c
        pangulu_cuda_interface.c
        pangulu_getrf_fp64_cuda.c
        pangulu_numeric.c
        pangulu_sptrsv_fp64.c
        pangulu_time.c
        pangulu_addmatrix_cuda.c
        pangulu_destroy.c
        pangulu_heap.c
        pangulu_preprocessing.c
        pangulu_ssssm_fp64.c
        pangulu_tstrf_fp64.c

        platforms/02_GPU/01_CUDA/000_CUDA/pangulu_cuda.cu
)

add_library(pangulu SHARED ${PANGULU_SRCS})
