CMAKE_MINIMUM_REQUIRED( VERSION 3.8 )
PROJECT(bzlib C)

set(LIB_DIR ${CMAKE_CURRENT_SOURCE_DIR}/../library/)
INCLUDE_DIRECTORIES(${LIB_DIR})
set(LIBRARY ${LIB_DIR}bin/libbzlib.so)

add_executable(bzip2 bzip2.c)
target_link_libraries(bzip2 ${LIBRARY})

add_executable(bzip2recover bzip2recover.c)
target_link_libraries(bzip2recover ${LIBRARY})