# RISC-V-BASED-MYTH
This repository contains my implementation of a 5-stage pipelined RISC-V CPU, built from the ground up using TL-Verilog. This project was the culmination of my learning in the RISC-V MYTH Workshop, conducted by VLSI System Design (VSD) and Redwood EDA.
# INTRODUCTION
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

# DEVELOPMENT WORKFLOW
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


