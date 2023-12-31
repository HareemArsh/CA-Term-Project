# CA-Term-Project

## 3-stage pipelined processor

A 3-stage pipelined processor is a type of microprocessor architecture that divides the execution of instructions into three distinct stages. The three stages typically include:

#### Fetch (IF - Instruction Fetch): Fetch the next instruction from memory.

#### Decode/Execute (ID/EX - Instruction Decode/Execute): Decode the instruction and perform any necessary calculations or logical operations.

#### Write Back (WB - Write Back): Write the result back to the register file or memory.

In a pipelined architecture, these stages are overlapped, allowing the processor to work on multiple instructions simultaneously. While one instruction is being fetched, the processor can decode another instruction, and a third instruction can be writing its result back.

Now, when you add CSR (Control and Status Register) support to a processor, it means that the architecture includes special registers (CSRs) that allow the processor's control and operational behavior to be modified or monitored by software (typically the operating system or privileged code). CSRs might be used for tasks like enabling or disabling interrupts, changing processor modes, or reading status information.

## Overview
This project is an implementation of a 3-stage pipelined processor with support for Control and Status Registers (CSRs). The processor is designed for efficient and parallel execution of instructions, enhancing overall performance. The inclusion of CSRs allows for improved control and monitoring of the processor's behavior.

### Features
3-Stage Pipeline: The processor employs a classic 3-stage pipeline architecture, including instruction fetch, instruction decode/execute, and write back stages. This design enhances instruction throughput and overall system performance.

### CSR Support:
Control and Status Registers are integrated into the processor, providing a mechanism for software to control various aspects of the processor and access important status information. This enables more flexibility and customization in handling different scenarios.

### RISC Architecture: 
The processor follows a Reduced Instruction Set Computing (RISC) architecture, focusing on a small, highly optimized set of instructions for efficient execution.

### Verilog Implementation: 
The project is implemented using Verilog, making it compatible with various FPGA (Field-Programmable Gate Array) platforms and easy to integrate into larger digital systems.

## Usage
### Simulation:
Use the provided testbenches to simulate the processor's behavior in a software environment. This helps in verifying the correctness and functionality of the design.

### Synthesis: 
The design is synthesizable for FPGA platforms. Follow the provided synthesis scripts or use your preferred synthesis tool to generate the bitstream for your target FPGA.

### Integration: 
Integrate the processor into your larger digital system or project. Ensure proper connections and interfaces with memory, peripherals, and other components.

## Contributions
Contributions are welcome! If you find bugs, have feature requests, or want to contribute improvements, please open an issue or submit a pull request.

## Instructions/Testcase:

Below are some example test cases for a 3-stage pipelined processor with CSR support using RISC-V assembly language. These test cases cover a range of instructions, including arithmetic operations, control flow, and CSR operations.

### Test Case 1: Arithmetic Operations
li a0, 5          # Load immediate 5 into a0
li a1, 7          # Load immediate 7 into a1
add a2, a0, a1    # a2 = a0 + a1 (addition)
sub a3, a1, a0    # a3 = a1 - a0 (subtraction)
mul a4, a2, a3    # a4 = a2 * a3 (multiplication)

### Test Case 2: Control Flow
beq a2, a3, label_equal  # Branch if a2 == a3
  li a5, 1         # Load immediate 1 into a5
  j label_end      # Jump to label_end

label_equal:
  li a5, 0         # Load immediate 0 into a5

label_end:

### Test Case 3: CSR Operations
li t0, 0x100      # Load immediate 0x100 into t0
csrw mstatus, t0  # Set mstatus (Machine Status) CSR to t0

# End of Test Cases
These test cases include a variety of instructions to exercise different aspects of the processor, such as arithmetic operations, control flow, and CSR operations. Adjust the instructions based on the specific instructions and CSR specifications supported by your processor



[A design diagram of project link of which should be attached in the README:] (https://drive.google.com/file/d/1XHxf7IS3_D_y3UqH5a-Dd581iqeFLX_J/view?usp=sharing)
