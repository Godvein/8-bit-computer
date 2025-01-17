# 8-Bit Computer Control Logic Module
 | ![Alt text](images/logisimfinal.png) |
 |:---------------------------------------:|
 | **Figure 1**: Circuit Diagram of Control Logic added to circuit in Logisim |
   

## Overview
The Control Logic Module is the brain of the 8-bit computer, responsible for generating control signals that orchestrate the operations of various components. This module uses an EEPROM to store the control signals for each microinstruction and a microinstruction counter to keep track of the current step in the instruction cycle.

## Components
1. **EEPROM**  
   - Stores the control signals for each microinstruction.  
   - Each address in the EEPROM corresponds to a unique microinstruction.  
   - Outputs the appropriate control signals based on the current address from the microinstruction counter.

2. **Microinstruction Counter**  
   - Keeps track of the current microinstruction being executed.  
   - Increments sequentially to step through the microinstructions.  
   - Can be reset or jumped to a specific address for handling loops or jumps in the program.

## Working Mechanism
1. **Fetching Control Signals**  
   - The microinstruction counter provides an address to the EEPROM.  
   - The EEPROM outputs the control signals associated with the given address.

2. **Executing Microinstructions**  
   - The control signals activate specific components (e.g., registers, ALU, bus) to perform operations like fetching, decoding, and executing instructions.

3. **Advancing the Microinstruction Counter**  
   - The microinstruction counter increments after each clock cycle, progressing to the next step in the control sequence.  
   - Conditional logic may be used to alter the counter's value for jumps or branches.

## Features
- **Flexible Programming**: The EEPROM allows for easy reprogramming of control signals to support new instructions or modify existing ones.  
- **Sequential Operation**: The microinstruction counter ensures orderly progression through the instruction cycle.  
- **Reusability**: The modular design allows the control logic to be adapted for other projects or expanded for more complex instruction sets.



