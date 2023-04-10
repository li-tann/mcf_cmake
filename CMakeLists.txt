cmake_minimum_required(VERSION 3.0.0)
project(mcf VERSION 0.1.0)

set(CMAKE_C_STANDARD 17)
set(CMAKE_C_EXTENSIONS on)
set(CMAKE_C_STANDARD_REQUIRED on)

add_executable(mcf
        bmp_image.h
        DISP_lib.c
        display.h
        m_ssp2_d_heap.c
        m_tri_init2.c
        mcf.c
        mcf2.h
        mssptr.c
        palsar.h
        rasterfile.h
        SWAP_io.c
        triangle.c
        triangle.h)
        # typedef_ISP.h)