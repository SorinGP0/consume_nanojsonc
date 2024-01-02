cmake_minimum_required(VERSION 3.26)
set(CMAKE_C_STANDARD 99)

project(clion_consume_library C)

add_subdirectory(ports)

#set(CMAKE_TOOLCHAIN_FILE "E:/upwork/saad/vcpkg/scripts/buildsystems/vcpkg.cmake"
#        CACHE STRING "Vcpkg toolchain file")

include("E:/upwork/saad/vcpkg/scripts/buildsystems/vcpkg.cmake")
find_package(nanodjsonc CONFIG REQUIRED)

target_link_libraries(clion_consume_library PRIVATE nanojsonc)
add_library(clion_consume_library library.c)







