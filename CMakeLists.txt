cmake_minimum_required (VERSION 2.6)
project (Face) 

set (Face_VERSION_MAJOR 1)
set (Face_VERSION_MINOR 1)

configure_file (
    "${PROJECT_SOURCE_DIR}/FaceConfig.h.in"
    "${PROJECT_BINARY_DIR}/FaceConfig.h"
)

include_directories("${PROJECT_BINARY_DIR}")

add_executable(Face face.cpp) 

install (TARGETS Face DESTINATION bin)
install (FILES "${PROJECT_BINARY_DIR}/FaceConfig.h" DESTINATION include)

