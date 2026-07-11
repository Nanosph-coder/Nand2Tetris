# Nand to Tetris Hardware Projects

*Completed as part of the **Week 3 Task** for **ArIES, IIT Roorkee***

## Overview
This repository contains the hardware implementation files for the initial projects of the Nand to Tetris curriculum, undertaken as the Week 3 task for ArIES at IIT Roorkee. The projects progress from elementary logic gates, through Boolean arithmetic, and into sequential logic and memory architectures for the Hack computer.

---

## Project 1: Elementary Logic Gates

### Objective
Build a typical set of elementary logic gates from a primitive `Nand` gate. These serve as the foundational building blocks for the architecture.

### Chips Implemented
* **Basic Gates:** `Not`, `And`, `Or`, `Xor`, `Mux`, `DMux`
* **16-bit Variants:** `Not16`, `And16`, `Or16`, `Mux16`
* **Multi-Way Variants:** `Or8Way`, `Mux4Way16`, `Mux8Way16`, `DMux4Way`, `DMux8Way`

---

## Project 2: Boolean Arithmetic

### Objective
Build a set of chips that carry out arithmetic addition, culminating in the construction of the ALU (Arithmetic-Logic Unit), which is the computational centerpiece of the CPU.

### Chips Implemented
* `HalfAdder`
* `FullAdder`
* `Add16`
* `Inc16`
* `ALU`

### Implementation Details
* **Dependencies:** Chip implementations in this section can use any of the chips built in Project 1, as well as earlier chips from Project 2.
* **The Hack ALU:** The ALU computes a 16-bit output (`out`) alongside two 1-bit status flags: `zr` (true if the output is zero) and `ng` (true if the output is negative).
* **Development Approach:** It is recommended to build the ALU in two stages:
    1. **Basic:** Compute the `out` value only (verify with `ALU-basic.tst` and `ALU-basic.cmp`).
    2. **Final:** Add the logic for the `zr` and `ng` flags (verify with `ALU.tst` and `ALU.cmp`).

---

## Project 3: Memory

### Objective
Build a Random Access Memory (RAM) unit, which is an addressable sequence of registers designed to hold n-bit values. This involves using gate logic to store bits persistently over time and locating (addressing) the specific memory register on which we wish to operate.

### Chips Implemented
* `Bit`
* `Register`
* `RAM8`
* `RAM64`
* `RAM512`
* `RAM4K`
* `RAM16K`
* `PC` (Program Counter)

### Implementation Details
* **Primitive:** The Data Flip-Flop (`DFF`) gate is considered primitive, so it is provided as a base and does not need to be implemented.
* **Dependencies:** Implementations can use any chips built in Projects 1, 2, and earlier chips in Project 3.
* **Folder Structure:** If using the desktop simulator, the project files are divided into two subfolders (`a` and `b`) for technical reasons. This structure must be maintained as-is without moving files between them.

---

## Testing and Verification
All chips are verified using the **Nand2Tetris Hardware Simulator** (Online IDE).

For every chip, the testing workflow relies on:
1. **`.hdl` (Hardware Description Language):** The implementation file containing your logic.
2. **`.tst` (Test Script):** Instructs the simulator on how to test the chip.
3. **`.cmp` (Compare File):** Contains the correct expected outputs.

**To Test:** Load the `.hdl` and `.tst` files into the simulator and run the script. The simulator will report an error if your actual outputs disagree with the desired outputs in the `.cmp` file.

---
*Reference: Based on the Nand to Tetris curriculum by Noam Nisan and Shimon Schocken.*
