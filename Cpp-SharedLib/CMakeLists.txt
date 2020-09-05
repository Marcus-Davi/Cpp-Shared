cmake_minimum_required(VERSION 3.8)
project(myshared)




add_library(mylib SHARED lib/mylib.cpp)
add_library(mylibs STATIC lib/mylib.cpp)
include_directories(lib)


add_executable(usinglocal src/main.cpp)
target_link_libraries(usinglocal mylib)
