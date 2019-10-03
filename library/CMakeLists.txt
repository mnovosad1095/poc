CMAKE_MINIMUM_REQUIRED( VERSION 3.8 )

PROJECT(bzlib C)

SET(bzlib_FILES  bzlib.c compress.c crctable.c blocksort.c
        decompress.c huffman.c main.c
        randtable.c bzlib.h bzlib_private.h )

set(LIBRARY_OUTPUT_PATH ../bin)
add_library(bzlib STATIC ${bzlib_FILES})
add_library(bzlib-shared SHARED ${bzlib_FILES})
set_target_properties(bzlib-shared PROPERTIES OUTPUT_NAME bzlib)