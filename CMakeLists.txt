cmake_minimum_required(VERSION 3.20)
project(cmake_ch32h417 C CXX ASM)

include("cmake/riscv-wch-elf.cmake")

add_subdirectory(Peripherial)
add_subdirectory(V3F)
add_subdirectory(V5F)