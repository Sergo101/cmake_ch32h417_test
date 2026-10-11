# CH32H417-CMake

Blink example for ch32h417 mcu.

This repo shows how to build dual core project for ch32h417 with cmake and debug in VSCode using gdb and openocd.

Cortex-debug run dual core in single workspace.

This example starts at nanoCH32H417 v1.0 board.

# Build requirements

cmake

ninja

riscv-wch-elf-gcc - can be found in MounRiver_Studio2\resources\app\resources\win32\components\WCH\Toolchain\RISC-V Embedded GCC12\bin

You should add path to compiler to PATH system variable or hardcode it in cmake/riscv-wch-elf.cmake and in .vscode/tools.json

# Debug requirements

WCH uses their oun version of openocd, so you should specify system variable WCH_OPENOCD or hardcode pathes just replace ${env:WCH_OPENOCD} with path to openocd.exe. Openocd can be found in MounRiver_Studio2\resources\app\resources\win32\components\WCH\OpenOCD\OpenOCD\bin

riscv-wch-elf-gdb is a part of WCH toolchain and path to it you can find in 'Build requirements'. 

# VSCode extensions requirements



Cortex-debug

Cmake

Cmake tools

Command Variable

# Build in VSCode using CMake extension

Press Ctrl+Shift+P, type CMake: Select Configure Preset

Click debug or whatever

Press Build button on lower panel