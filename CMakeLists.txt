cmake_minimum_required(VERSION 3.15)

set(CMAKE_EXPORT_COMPILE_COMMANDS true)

project(libpng LANGUAGES C)

set(CMAKE_C_STANDARD 99)

add_library(png STATIC
	png.c
	pngset.c
	pngget.c
	pngrutil.c
	pngtrans.c
	pngwutil.c
	pngread.c
	pngrio.c
	pngwio.c
	pngwrite.c
	pngrtran.c
	pngwtran.c
	pngmem.c
	pngerror.c
	pngpread.c
)
target_compile_options(png PUBLIC -Wall -O3 -funroll-loops)
target_include_directories(png PUBLIC ../zlib-1.2.1)
