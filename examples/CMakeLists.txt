CMAKE_MINIMUM_REQUIRED( VERSION 3.8 )
PROJECT(bzlib C)


INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}../library/bin)
set(LIB_DIR ${CMAKE_CURRENT_SOURCE_DIR}../library/bin)
set(LIBRARY ${LIB_DIR}/bzlib.so)

add_executable(bzip2 bzip2.c)
target_link_libraries(bzip2 ${LIBRARY})