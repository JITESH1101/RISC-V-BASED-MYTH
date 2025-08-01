# RISC-V-BASED-MYTH
This repository contains my implementation of a 5-stage pipelined RISC-V CPU, built from the ground up using TL-Verilog. This project was the culmination of my learning in the RISC-V MYTH Workshop, conducted by VLSI System Design (VSD) and Redwood EDA.
# Introduction
This workshop was a deep dive into the full stack of computer architecture, from software to hardware. Key takeaways include:

- RISC-V ISA:- A thorough understanding of the RISC-V instruction set and its design philosophy.

- Software Development:- Writing, compiling, and debugging C and Assembly programs for a RISC-V target.

- Simulation & Verification:- Using industry-standard tools like Spike to simulate program execution and objdump to analyze binary files.

- Digital Design with TL-Verilog:- Mastering Transaction-Level Verilog on the MakerChip IDE to describe complex hardware behavior efficiently.

- CPU Microarchitecture:- Designing and integrating essential CPU components, including:
 
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

- RISC-V ISA: Learned about the base integer ISA (RV64I), its extensions, register width (XLEN), and the 32 integer registers.

- GNU Compiler Toolchain: Explored the compilation flow from C source code to machine code: Preprocessor -> Compiler -> Assembler -> Linker.

Hands-on Lab Work:-

- Compiled C programs using  riscv64-unknown-elf-gcc  with different optimization flags (-O1, -Ofast).

- Generated and analyzed assembly code using riscv64-unknown-elf-objdump to understand how C constructs translate to machine instructions.

- Simulated the compiled object files using the Spike ISA simulator.

- Used Spike's interactive debug mode to step through programs, set breakpoints at specific program counter (PC) addresses, and inspect the state of registers (like a0, sp).

- Explored integer number representation and data type limitations by modifying C code to handle 64-bit signed and unsigned integers.

# Day 2: Application Binary Interface (ABI) and Verification Flow

This day bridged the gap between high-level software and the underlying hardware conventions.

Core Concepts:

- Application Binary Interface (ABI): Understood the ABI as a set of rules for interoperability, defining how functions are called, arguments are passed, and values are returned.

- RISC-V Calling Conventions: Learned the specific ABI names for the 32 general-purpose registers (a0-a7 for arguments, sp for stack pointer, etc.).

Hands-on Lab Work:

- Created a hybrid program by writing a custom function in RISC-V Assembly (.S file) and calling it from a C program (.c file).

- This exercise demonstrated practical use of the ABI for passing arguments to and receiving results from the assembly function.

- Used the Spike debugger to trace the execution flow between C and assembly, verifying that registers were used according to the calling conventions.

- Introduced the basic hardware verification flow using iverilog and created shell scripts (.sh) to automate the compilation of C programs for a 32-bit RISC-V target (rv32im).

# Day 3: Introduction to Hardware Design with TL-Verilog

The focus shifted from software to hardware, introducing a modern approach to digital design.

Core Concepts:

- TL-Verilog: Introduced as a high-level abstraction over SystemVerilog that simplifies hardware design, reduces code, and minimizes bugs.

- Transaction-Level Design: Learned to think of designs as pipelines where data flows through stages.

- Makerchip IDE: Became familiar with the browser-based IDE for writing, simulating, and visualizing TL-Verilog designs.

- Validity: Learned about the $valid signal, a key feature in TL-Verilog for cleaner design, easier debugging, and implicit clock gating.

Hands-on Lab Work:

- Combinational Logic: Implemented basic logic gates (inverter, adder) and more complex circuits like a multiplexer and an arithmetic calculator.

- Sequential Logic: Built sequential circuits, including a counter and a Fibonacci number generator, using pipelined assignments.

- Pipelining: Implemented multi-stage logic by replicating a circuit diagram directly in TL-Verilog, leveraging its intuitive pipeline (|pipe) syntax.

- Applying Validity: Enhanced the calculator designs to use the validity feature, observing how it controlled the flow of valid data in the simulation waveforms.

# Day 4: Designing a Single-Cycle RISC-V CPU Microarchitecture

With a strong foundation in TL-Verilog, we began constructing the core of the RISC-V CPU.

Core Concepts:

- CPU Microarchitecture: Outlined the essential building blocks of a simple processor.

- Fetch-Decode-Execute Cycle: Implemented the logic for the fundamental stages of instruction processing.

- RISC-V Instruction Formats: Learned to decode the different instruction types (R, I, S, B, U, J) based on their opcode and function fields.

Hands-on Lab Work:

- Designed and implemented the following CPU components in TL-Verilog:

- Program Counter (PC): With logic to increment sequentially or jump to a new address.

- Instruction Memory: To fetch instructions based on the PC.

- Instruction Decoder: To parse the fetched instruction and generate control signals.

- Register File: With two read ports and one write port.

- Arithmetic Logic Unit (ALU): To perform arithmetic and logical operations.

- Control Logic: To handle conditional branches by checking ALU outputs.


# Day 5: Pipelining the CPU and Completing the RV32I Core

The final day focused on optimizing the CPU with a pipeline and completing the instruction set.

Core Concepts:

- Pipelined CPU: Understood the benefits of pipelining and how it improves instruction throughput.

- Load and Store Operations: Learned how to interact with a data memory module.

Hands-on Lab Work:

- Converting to a Pipeline: Effortlessly transformed the single-cycle CPU design into a multi-stage pipelined architecture using TL-Verilog's concise syntax.

- Adding Data Memory: Integrated a Data Memory module to support load and store instructions, enabling the CPU to read from and write to memory.

Completing the RV32I ISA:

- Expanded the instruction decoder and control logic to handle all remaining instructions in the base integer set.

- Added support for unconditional jumps (J-type instructions).

- Finalized the ALU operations required by the full instruction set.

# Final RV32I Core
![WhatsApp Image 2025-07-31 at 01 52 38_e031561d](https://github.com/user-attachments/assets/068b5a80-58ef-4430-b366-cc84b78bd34a)





