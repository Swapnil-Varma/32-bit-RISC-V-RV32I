# 32-bit RISC-V (RV32I) Processor Core

## Overview

This project focuses on the design and development of a **32-bit RISC-V RV32I processor core** using **Verilog HDL** and **Xilinx Vivado**.

The processor is being developed at the **RTL (Register Transfer Level)** to explore processor architecture, datapath and control-path design, instruction execution, functional verification, and FPGA implementation.

**Project Status: 🚧 Ongoing**

---

## Objectives

* Design a 32-bit RISC-V processor based on the **RV32I base integer instruction set**.
* Develop the processor architecture using modular, synthesizable Verilog RTL.
* Implement the datapath, control unit, ALU, register file, and instruction handling logic.
* Verify processor functionality using simulation and testbenches.
* Synthesize and analyze the design using Xilinx Vivado.
* Target the design for implementation on an **Artix-7 FPGA**.

---

## Processor Architecture

The processor consists of the following major blocks:

```text
                    +-------------------+
                    | Program Counter   |
                    +---------+---------+
                              |
                              v
                    +-------------------+
                    | Instruction Memory|
                    +---------+---------+
                              |
                              v
                    +-------------------+
                    | Instruction       |
                    | Decoder           |
                    +---------+---------+
                              |
                +-------------+-------------+
                |                           |
                v                           v
        +---------------+           +---------------+
        | Register File |           | Control Unit  |
        +-------+-------+           +---------------+
                |
                v
          +-----------+
          |    ALU    |
          +-----+-----+
                |
          +-----+-----+
          |           |
          v           v
    +-----------+  +-----------+
    | Data      |  | Writeback |
    | Memory    |  | Logic     |
    +-----------+  +-----------+
```

---

## RISC-V ISA

The project targets the **RV32I base integer instruction set**.

The processor is being developed to support the following instruction categories:

### Arithmetic & Logical Instructions

* ADD
* SUB
* AND
* OR
* XOR
* SLT
* SLTU

### Immediate Instructions

* ADDI
* ANDI
* ORI
* XORI
* SLTI

### Memory Instructions

* LW
* SW

### Branch Instructions

* BEQ
* BNE
* BLT
* BGE
* BLTU
* BGEU

### Jump Instructions

* JAL
* JALR

### Upper Immediate Instructions

* LUI
* AUIPC

Instruction support and verification will be expanded progressively during development.

---

## RTL Modules

The processor is being developed using modular RTL components, including:

* **Program Counter**
* **Instruction Memory**
* **Instruction Decoder**
* **Control Unit**
* **Register File**
* **Arithmetic Logic Unit (ALU)**
* **Immediate Generator**
* **Branch and Jump Logic**
* **Data Memory**
* **Write-Back Logic**
* **Top-Level RISC-V Core**

The module organization may evolve as additional processor features are implemented.

---

## Design Flow

The project follows a standard FPGA RTL development workflow:

```text
Verilog RTL Design
        ↓
Module Integration
        ↓
Testbench Development
        ↓
Functional Simulation
        ↓
Debugging & Verification
        ↓
Synthesis
        ↓
Implementation
        ↓
Timing & Resource Analysis
        ↓
FPGA Implementation
```

---

## Verification

The processor is being verified using **Verilog testbenches** and **Vivado Simulator**.

Verification includes:

* Instruction decoding
* ALU operations
* Register read/write operations
* Immediate value generation
* Program counter operation
* Branch and jump operations
* Load/store operations
* Instruction sequencing
* Reset functionality

As development progresses, instruction-level and self-checking verification will be added.

---

## FPGA Implementation

The processor is being developed using **Xilinx Vivado** and is targeted toward an **Xilinx Artix-7 FPGA** platform.

The FPGA implementation will be evaluated based on:

* LUT utilization
* Flip-Flop utilization
* Block RAM utilization
* Timing performance
* Maximum operating frequency
* Overall hardware resource utilization

---

## Tools & Technologies

| Category           | Technology       |
| ------------------ | ---------------- |
| HDL                | Verilog          |
| Processor ISA      | RISC-V RV32I     |
| FPGA Tool          | Xilinx Vivado    |
| Target FPGA        | Xilinx Artix-7   |
| Simulation         | Vivado Simulator |
| Design Methodology | RTL Design       |

---

## Project Structure

```text
RISC-V-Processor/
│
├── RTL/
│   ├── alu.v
│   ├── register_file.v
│   ├── control_unit.v
│   ├── instruction_decoder.v
│   ├── immediate_generator.v
│   ├── program_counter.v
│   ├── instruction_memory.v
│   ├── data_memory.v
│   └── riscv_core.v
│
├── Testbench/
│   └── riscv_core_tb.v
│
├── Constraints/
│   └── basys3.xdc
│
├── Simulation/
│   └── simulation_results/
│
├── Documentation/
│   └── architecture/
│
└── README.md
```

> The project structure will be updated as development progresses.

---

## Future Work

Planned improvements include:

* Complete RV32I instruction-set implementation
* Comprehensive instruction verification
* Self-checking testbenches
* RISC-V assembly program execution
* FPGA hardware validation
* Timing optimization
* Resource optimization
* Performance evaluation
* 5-stage pipelined architecture
* Data hazard detection
* Forwarding and pipeline stalls
* Branch handling

---

## Learning Outcomes

This project provides hands-on experience in:

* RTL Design
* Verilog HDL
* Digital System Design
* Processor Architecture
* RISC-V ISA
* Datapath and Control-Path Design
* Functional Verification
* FPGA Design Flow
* Hardware Resource Analysis
* Xilinx Vivado

---

## Project Status

### 🚧 Currently Under Development

The processor is being developed incrementally, starting with the fundamental **RV32I datapath and control logic**, followed by instruction execution, functional verification, synthesis, and FPGA implementation.

---

## Author

**Swapnil Varma**

Electronics Engineering
The Maharaja Sayajirao University of Baroda

### Areas of Interest

* VLSI Design
* RTL Design
* FPGA Design
* Digital IC Design
* Processor Architecture
* RISC-V
* Hardware Verification

---

## License

This project is intended for **educational and academic purposes**.
