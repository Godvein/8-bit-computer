# Registers in the 8-Bit Computer  
 | ![Alt text](images/registers.png) |
 |:---------------------------------------:|
 | **Figure 1**: Circuit Diagram of register added to circuit in logisim |
   

This 8-bit computer design includes **three registers**:  

1. **Register A** (General-Purpose Register)  
2. **Register B** (General-Purpose Register)  
3. **Instruction Register** (Dedicated for holding instructions during execution)  

These registers play a crucial role in the computer's operation, enabling efficient data processing, storage, and execution.

---

## What Are Registers?  

Registers are small, fast storage units located within the CPU that temporarily hold data and instructions during computation. They are essential for performing operations and facilitating data flow between the CPU and memory.  

---

## The Three Registers  

### 1. **Register A**  
- **Purpose**: Used as a general-purpose register for arithmetic and logical operations.  
- **Width**: 8 bits (can hold values from 0 to 255 in decimal).  
- **Interaction**:  
  - Can store data loaded from memory or another register.  
  - Works with the Arithmetic Logic Unit (ALU) for computations.  
  - Often serves as an accumulator for results.  

---

### 2. **Register B**  
- **Purpose**: Another general-purpose register that complements Register A.  
- **Width**: 8 bits.  
- **Interaction**:  
  - Acts as an operand source for the ALU.  
  - Can exchange data with memory or other registers.  
  - Enables efficient data manipulation when paired with Register A.  

---

### 3. **Instruction Register**  
- **Purpose**: Holds the current instruction fetched from memory, which is then decoded and executed by the control unit.  
- **Width**: 8 bits (matches the instruction size in this computer).  
- **Interaction**:  
  - Receives instructions from the memory during the fetch phase.  
  - Passes the decoded instructions to the control unit for execution.  

---

## Why Use Multiple Registers?  

1. **Efficiency**:  
   Registers operate much faster than memory, allowing for quick data retrieval and storage.  

2. **Parallel Operations**:  
   Having multiple registers enables simultaneous data storage and processing, improving overall performance.  

3. **Simplifies Computation**:  
   Registers reduce the need for frequent memory access, which can be slow.  

---

## How Registers Work in the 8-Bit Computer  

1. **Register A** and **Register B**:  
   - Data is loaded into these registers from memory.  
   - The ALU performs operations like addition or subtraction using these registers.  
   - Results can be stored back in Register A or written to memory.  

2. **Instruction Register**:  
   - Fetches instructions from ROM.  
   - Sends the opcode to the control unit to determine the operation.  
   - Ensures smooth execution by temporarily holding the current instruction.  

---

## Register Example in Action  

### Addition Operation Example:  
1. Load value `5` into Register A.  
2. Load value `3` into Register B.  
3. ALU performs `Register A + Register B` and stores the result (`8`) back into Register A.  

---

## Acknowledgments  

Special thanks to **Ben Eater**, whose work on 8-bit computers inspired this project. The insights gained from his tutorials were instrumental in understanding and designing this computer.  

---

## License  

This project is licensed under the [MIT License](LICENSE).  

Feel free to use and modify it for learning or extending your projects!  

---

