# CA-Term-Project

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
