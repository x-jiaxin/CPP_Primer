cmake_minimum_required(VERSION 3.24)
project(CPP_Primer)

set(CMAKE_CXX_STANDARD 20)
file(GLOBAL head_files ${PROJECT_SOURCE_DIR}/include/*)
foreach (file ${head_files})
    include_directories(file)
    message()
endforeach ()

add_executable(CPP_Primer main.cpp)
