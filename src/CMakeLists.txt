cmake_minimum_required(VERSION 3.24)

file(GLOB head_files ${PROJECT_SOURCE_DIR}/include/*)
foreach (file ${head_files})
    include_directories(${file})
endforeach ()

file(GLOB src_dirs ${PROJECT_SOURCE_DIR}/src/*)
foreach (file ${src_dirs})
    aux_source_directory(${file} SRCLIST)
endforeach ()

add_library(SRC ${SRCLIST})