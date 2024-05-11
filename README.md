# stages-of-pipelining
# CPU Datapath

This repository contains Verilog code for a simple CPU datapath. The CPU consists of various modules interconnected to form a datapath for executing instructions. Below is an overview of the modules and their functionalities:

## Modules

### Program_counter
- Responsible for managing the program counter.

### Instruction_memory
- Represents the instruction memory of the CPU.

### pc_Adder
- Adds 4 to the current program counter.

### IFIDPipelineRegister
- Pipeline register between the Instruction Fetch (IF) and Instruction Decode (ID) stages.

### Control_unit
- Controls the execution of instructions based on opcode and function codes.

### regrtMultiplexer
- Selects destination register based on the value of regrt.

### registerFile
- Represents the register file of the CPU.

### immediateExtender
- Extends immediate values to 32 bits.

### IDEXEPipelineRegister
- Pipeline register between the Instruction Decode (ID) and Execute (EX) stages.

### ALU_Mux
- Selects ALU input based on aluimm.

### Alu
- Arithmetic Logic Unit (ALU) for executing arithmetic and logic operations.

### EXEMEM_Pipeline_Register
- Pipeline register between the Execute (EX) and Memory (MEM) stages.

### Data_Memory
- Represents the data memory of the CPU.

### MEMWB_Pipeline_Register
- Pipeline register between the Memory (MEM) and Write Back (WB) stages.

### WBMux
- Selects write-back data based on wm2reg.

### muxfwda
- Forwards data from various pipeline stages based on the value of fwda.

### muxfwdb
- Forwards data from various pipeline stages based on the value of fwdb.

### Datapath
- Top-level module that instantiates all other modules and connects them together to form the CPU datapath.

## How to Use

To use this CPU datapath in your project, follow these steps:
1. Clone this repository.
2. Instantiate the `Datapath` module in your Verilog code.
3. Connect the necessary input and output ports of the `Datapath` module to other modules or external components as per your requirements.
4. Simulate or synthesize your Verilog design.

## Contributors

- Designer: Aaron Amspacker
