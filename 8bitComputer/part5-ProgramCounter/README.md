# Program Counter (PC) - 8-Bit Computer
 | ![Alt text](images/programcounter.png) |
 |:---------------------------------------:|
 | **Figure 1**: Circuit Diagram of the program counter added to circuit in logisim |
   


## Overview
The Program Counter (PC) is a crucial component in this 8-bit computer, responsible for managing the sequential execution of instructions. It keeps track of the memory address of the next instruction to be fetched and executed, ensuring the computer follows the program flow correctly.

## Design and Features
### 8-Bit Address Space
- **Capacity**: As the computer uses an 8-bit address bus, the Program Counter can address up to **256 memory locations** (0x00 to 0xFF).
- **Sequential Execution**: The PC automatically increments after each instruction fetch, ensuring the computer processes instructions in order.

### Core Operations
The Program Counter supports the following operations:
1. **Increment**:
   - The PC increments by 1 after fetching an instruction, pointing to the next memory address.
   - This is the default behavior during normal program execution.

2. **Jump**:
   - The PC can be manually loaded with a new address, enabling the execution to jump to a specific instruction in memory.
   - This is used for branching, subroutine calls, and loops.

3. **Reset**:
   - The PC can be reset to address 0x00, typically during the initial power-on or program start.

### Integration with the Bus
- **Output to Address Bus**: The PC places its current value onto the address bus to fetch the next instruction from memory.
- **Input from Data Bus**: In jump or branch operations, the PC can load a new address directly from the data bus, allowing dynamic control of program flow.

## How It Works
1. During each clock cycle, the PC sends its value to the address bus, directing the memory to provide the instruction at that address.
2. After the instruction is fetched, the PC either:
   - Increments to the next address for sequential execution.
   - Loads a new address (if a jump or branch operation is triggered).

### Example Usage
- **Sequential Execution**: If the PC starts at 0x00, it fetches instructions from 0x00, 0x01, 0x02, and so on.
- **Jump/Branch**: If a `JUMP` instruction is encountered, the PC loads the target address (e.g., 0x50) and begins fetching from there.

## Key Benefits
- **Control Flow Management**: The PC ensures instructions are fetched and executed in the correct sequence.
- **Flexibility**: Jump and branch capabilities allow for more complex program logic, including loops and conditional execution.
- **Integration**: Its direct connection to the address bus enables seamless communication with RAM and other components.

The Program Counter is a fundamental element that orchestrates the execution flow of programs in this 8-bit computer.

