# RISC-MIPS32-Microprocessor
# 5-Stage Pipelined RISC MIPS32 Processor

This repository contains the implementation of a 5-stage pipelined RISC (Reduced Instruction Set Computer) processor based on the MIPS32 architecture. The design executes instructions in a pipelined manner, significantly improving throughput compared to a single-cycle processor.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Architecture](#architecture)
- [Pipeline Stages](#pipeline-stages)
- [Instruction Set](#instruction-set)
- [Installation](#installation)
- [Usage](#usage)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

## Introduction

MIPS32 is a RISC architecture widely studied in computer architecture courses. This project implements a 5-stage pipelined processor following the MIPS32 instruction set, which increases CPU instruction throughput by allowing multiple instructions to be processed simultaneously across different stages.

## Features

- **5-Stage Pipeline**: Includes stages for Instruction Fetch (IF), Decode (ID), Execute (EX), Memory Access (MEM), and Write-back (WB).
- **Hazard Detection**: Implements methods for handling data, control, and structural hazards.
- **Data Forwarding**: Utilizes data forwarding to resolve data hazards efficiently.
- **Branch Prediction**: Incorporates a basic branch prediction mechanism to reduce the penalty of control hazards.
- **MIPS32 Instruction Support**: Implements a subset of the MIPS32 instruction set.

## Architecture

The processor architecture is based on a 5-stage pipeline, where each stage is responsible for a different aspect of instruction processing:

1. **Instruction Fetch (IF)**: Fetches instructions from memory using the Program Counter (PC).
2. **Instruction Decode (ID)**: Decodes instructions and reads necessary registers; performs sign extension if required.
3. **Execute (EX)**: Carries out arithmetic and logical operations using the ALU; computes effective addresses for memory access instructions.
4. **Memory Access (MEM)**: Accesses data memory for load/store operations.
5. **Write-back (WB)**: Writes the computed result back to the register file.

## Pipeline Stages

- **Instruction Fetch (IF)**: Retrieves instructions from instruction memory based on the PC, which is updated to the next instruction.
- **Instruction Decode (ID)**: Decodes fetched instructions and reads operands from the register file; performs sign extension as needed.
- **Execute (EX)**: Executes arithmetic or logical operations using the ALU; computes effective addresses for memory access.
- **Memory Access (MEM)**: Handles memory read/write operations for load and store instructions.
- **Write-back (WB)**: Writes the result back to the destination register in the register file.

## Instruction Set

This processor supports a subset of the MIPS32 instruction set to demonstrate pipelined execution and hazard management.

## Installation

To install and run the project:

1. Clone the repository: 
   ```bash
   git clone https://github.com/yourusername/5-stage-pipelined-mips32.git


