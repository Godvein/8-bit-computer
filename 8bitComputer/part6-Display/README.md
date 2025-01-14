# 8-Bit Computer Display Module

## Overview
The Display Module in this 8-bit computer is designed to visually represent data processed by the system. It utilizes three ROM chips, each pre-programmed to handle a specific digit, three 7-segment displays for output, and an output register to drive the display.

## Components
1. **ROM Chips (3x)**  
   - Each ROM is programmed to output the corresponding segment configurations for a single digit.
   - The ROMs work together to display multi-digit numbers by handling one digit each.

2. **7-Segment Displays (3x)**  
   - These are used to visually represent the digits.  
   - Each 7-segment display corresponds to one ROM chip and shows the decoded digit.

3. **Output Register**  
   - Serves as the intermediary between the computer's bus and the display.  
   - Holds the data temporarily before sending it to the 7-segment displays, ensuring stable output.

## Working Mechanism
1. **Input to ROMs**  
   - Data from the bus is fed into the ROMs, which interpret the input as a specific digit.

2. **Digit Encoding**  
   - Each ROM outputs the appropriate segment data for its assigned digit.

3. **Register and Display**  
   - The output register stores the segment data temporarily.  
   - The data is then sent to the 7-segment displays, which light up the corresponding segments to form the desired digits.

## Features
- **Separation of Digits**: Each ROM is responsible for a single digit, simplifying programming and debugging.  
- **Stable Output**: The use of an output register ensures that the display does not flicker or show incomplete data.  
- **Scalability**: This design allows for easy expansion to support more digits by adding additional ROMs, registers, and displays.  
