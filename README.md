# RISC-V Pipelined Processor Hazard Unit

## Introduction
This repository contains the advanced implementation of a RISC-V pipelined processor with a focus on handling hazards through a Hazard Unit. The processor is designed to execute a subset of the RISC-V instruction set without the need for manual insertion of `nop` instructions.

## Project Structure
- `project06.dig`: The top-level digital circuit file for the pipelined processor.
- `.hex` files: Hexadecimal representations of machine code for testing the processor.

## Features
- **5-Stage Pipeline**: Implements a basic 5-stage instruction pipeline including IF, ID, EX, MEM, and WB stages with pipeline registers.
- **Hazard Unit**: Handles data hazards with register forwarding, stalls for memory reads, and flushes for control hazards.
- **RAM Support**: Includes support for `lw` and `sw` instructions.
- **Disassembler**: An ASCII-based disassembler for debugging and verification.

## Enhancements
The processor has been enhanced to include:
- **Data Path Additions**: New datapath lines for forwarding values from MEM and WB stages to the EX stage.
- **Register Forwarding**: Implementation of MUXes in the EX stage for register forwarding.
- **Stalling Mechanism**: Logic to stall the pipeline when necessary, particularly for memory reads.
- **Pipeline Flushing**: Capability to flush the pipeline to handle branches and jumps.

## Usage
To run the processor with a program:
1. Open the `project06.dig` file in Digital.
2. Load the corresponding `.hex` file into the instruction memory.
3. Run the simulation and observe the processor's behavior.

## Testing
The processor is tested using provided machine code programs that illustrate different hazard scenarios:
- `04-add-fwd.s`: Tests data hazards and register forwarding.
- `05-ld-stl.s`: Tests stalling for memory reads.
- `06-jal-fls.s`: Tests flushing for control hazards.


## Acknowledgments
I would like to express my gratitude to **Professor Greg Benson** for his guidance and support throughout the development of this project.

## Additional Resources
- To view and interact with `.dig` files, download and install Digital from Digital Logic Simulator. https://github.com/hneemann/Digital
