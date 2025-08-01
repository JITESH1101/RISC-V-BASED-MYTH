# RISC-V-BASED-MYTH
This repository contains my implementation of a 5-stage pipelined RISC-V CPU, built from the ground up using TL-Verilog. This project was the culmination of my learning in the RISC-V MYTH Workshop, conducted by VLSI System Design (VSD) and Redwood EDA.
# Introduction
This workshop was a deep dive into the full stack of computer architecture, from software to hardware. Key takeaways include:

RISC-V ISA:- A thorough understanding of the RISC-V instruction set and its design philosophy.

Software Development:- Writing, compiling, and debugging C and Assembly programs for a RISC-V target.

Simulation & Verification:- Using industry-standard tools like Spike to simulate program execution and objdump to analyze binary files.

Digital Design with TL-Verilog:- Mastering Transaction-Level Verilog on the MakerChip IDE to describe complex hardware behavior efficiently.

CPU Microarchitecture:- Designing and integrating essential CPU components, including:
 
 1. Register File
 
 2. Arithmetic Logic Unit (ALU)
 
 3. Control Logic
 
 4. A complete 5-Stage Pipeline

# Development Workflow
The project followed a structured, incremental approach:

1. C Programming: Wrote simple algorithms in C.

2. Simulation: Compiled the C code and simulated its execution on the RISC-V Spike simulator.

3. Assembly Translation: Studied the corresponding RISC-V assembly code to understand the hardware-software contract.

4. RTL Design: Began hardware implementation in TL-Verilog, starting with basic components.

5. Integration & Pipelining: Assembled the components into a functional CPU and implemented a 5-stage pipeline to optimize performance.

# Tech Stack

Languages: C, RISC-V Assembly, TL-Verilog

Architecture: RISC-V (RV32I)

Tools: GCC RISC-V Toolchain, Spike, objdump, MakerChip IDE

# Day 1: Software Toolchain and ISA Exploration

The first day focused on understanding the RISC-V ecosystem from a software perspective.

Core Concepts:-

1. RISC-V ISA: Learned about the base integer ISA (RV64I), its extensions, register width (XLEN), and the 32 integer registers.

2. GNU Compiler Toolchain: Explored the compilation flow from C source code to machine code: Preprocessor -> Compiler -> Assembler -> Linker.

Hands-on Lab Work:-

1. Compiled C programs using riscv64-unknown-elf-gcc with different optimization flags (-O1, -Ofast).

2. Generated and analyzed assembly code using riscv64-unknown-elf-objdump to understand how C constructs translate to machine instructions.

3. Simulated the compiled object files using the Spike ISA simulator.

4. Used Spike's interactive debug mode to step through programs, set breakpoints at specific program counter (PC) addresses, and inspect the state of registers (like a0, sp).

5. Explored integer number representation and data type limitations by modifying C code to handle 64-bit signed and unsigned integers.



