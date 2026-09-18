# 32-bit Pipelined RISC Processor

## Overview

This project presents the design and simulation of a 32-bit RISC processor using Verilog HDL.

The processor uses a five-stage instruction pipeline to allow multiple instructions to be processed at different stages of execution at the same time. This demonstrates the basic concepts of processor datapath design, instruction execution, and pipelining.

## Pipeline Architecture

The processor is divided into five main stages:

1. **Instruction Fetch (IF)**  
   Fetches the instruction from instruction memory and updates the program counter.

2. **Instruction Decode (ID)**  
   Decodes the instruction and obtains the required register values.

3. **Execute (EX)**  
   Performs arithmetic or logical operations using the ALU.

4. **Memory Access (MEM)**  
   Handles memory read and write operations when required.

5. **Write Back (WB)**  
   Writes the calculated result back into the register file.

## Features

- 32-bit RISC processor architecture
- Five-stage instruction pipeline
- Verilog HDL implementation
- Arithmetic and logical instruction support
- Memory-related instruction handling
- Control-flow instruction support
- Simulation using Verilog testbenches
- Verification using different instruction sequences

## Project Structure

```text
32-bit-Pipelined-RISC-Processor/
│
├── README.md
├── five_stage_cpu_mips32.v
├── arithmetic_testbench.v
├── memory_testbench.v
└── loop_control_testbench.v

**Working Principle**
Instructions move through the five pipeline stages in sequence:
IF → ID → EX → MEM → WB
While one instruction is being executed, other instructions can simultaneously occupy the preceding or following stages. This improves instruction throughput compared with a non-pipelined processor.

**Verification**
The design can be tested using Verilog simulation.
The testbenches can be used to verify:
Arithmetic operations
Register operations
Load and store operations
Program execution
Loop-based operations
Correct movement of instructions through the pipeline

**Tools Used**
Verilog HDL
Verilog simulator

**Learning Outcomes**
Through this project, the following concepts are explored:
RISC processor architecture
MIPS-style instruction execution
CPU datapath design
Five-stage pipelining
Verilog HDL
Testbench development
Digital processor simulation

**Applications**
Pipelined processor concepts are useful in:
CPU architecture
Embedded processor design
FPGA-based processor development
Digital system design
Computer architecture research

**Future Improvements**
Possible improvements include:
Pipeline hazard detection
Data forwarding
Branch handling
Additional instruction support
Improved memory architecture
FPGA implementation

**Conclusion**
This project demonstrates the design of a 32-bit pipelined RISC processor using Verilog HDL. The five-stage pipeline provides a practical way to understand how modern processors divide instruction execution into multiple stages and process several instructions concurrently.
