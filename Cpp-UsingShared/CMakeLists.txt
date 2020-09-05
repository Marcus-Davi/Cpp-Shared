cmake_minimum_required(VERSION 3.8)
project(usingmylib)

find_library(customlib mylib PATHS "../Cpp-SharedLib/build" REQUIRED)


include_directories("../Cpp-SharedLib/lib")

add_executable(main src/main.cpp)
# link_directories("../Cpp-SharedLib/build")


message(STATUS "CMAKE DIR : " ${CMAKE_SOURCE_DIR})
message(STATUS "LIB DIR : " ${customlib})

#target_link_libraries(main "${CMAKE_SOURCE_DIR}/libmylib.so")
target_link_libraries(main ${customlib})

