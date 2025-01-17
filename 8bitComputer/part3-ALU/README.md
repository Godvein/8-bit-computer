# Arithmetic Logic Unit (ALU) - 8-Bit Computer
 | ![Alt text](images/alu.png) |
 |:---------------------------------------:|
 | **Figure 1**: Circuit Diagram of ALU added to circuit in logisim |
   

## Overview
The ALU (Arithmetic Logic Unit) is a critical component of this 8-bit computer. It is responsible for performing arithmetic operations like addition and subtraction. The design focuses on simplicity and direct integration with the registers to ensure seamless operation.

## Design and Features
### 8-Bit Adder
At the core of the ALU is an 8-bit adder, which performs the primary arithmetic operations. It takes two 8-bit inputs and outputs their sum. 

### 2's Complement for Subtraction
To handle subtraction, the ALU leverages the 2's complement method. An XOR gate is used to invert the second operand when performing a subtraction operation:
- The XOR gate flips the bits of the second operand if a control signal indicates subtraction.
- The result, along with a carry-in of `1`, is processed by the adder to compute the subtraction as an addition of the first operand and the 2's complement of the second operand.

This design ensures efficient handling of both positive and negative values.

### Register Integration
The ALU is directly connected to the 8-bit registers:
- **Input**: The ALU receives its operands from the two general-purpose registers.
- **Output**: The result of the operation is sent back to one of the registers or stored for further processing.

The instruction register provides control signals to dictate the type of operation (addition or subtraction) the ALU performs.

## Operation Flow
1. **Addition**: Both operands are fed directly into the adder, which outputs their sum.
2. **Subtraction**: The XOR gate inverts the second operand (based on a control signal) to generate its 2's complement. This result, combined with the first operand, is processed by the adder to produce the difference.

### Benefits of This Design
- Simple yet robust mechanism for basic arithmetic.
- Direct integration with registers ensures minimal delay and efficient data handling.
- The 2's complement approach simplifies hardware requirements for subtraction.

This ALU design is a foundational element of the 8-bit computer, ensuring it can perform essential arithmetic operations effectively while maintaining simplicity.

