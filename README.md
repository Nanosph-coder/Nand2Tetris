# Nand to Tetris Hardware Projects

## Overview
This repository contains the hardware implementation files for the initial projects of the Nand to Tetris curriculum. The projects progress from elementary logic gates to a fully functional Arithmetic-Logic Unit (ALU) for the Hack computer architecture.

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

## Testing and Verification
All chips are verified using the **Nand2Tetris Hardware Simulator** (Desktop or Online IDE).

For every chip, the testing workflow relies on:
1. **`.hdl` (Hardware Description Language):** The implementation file containing your logic.
2. **`.tst` (Test Script):** Instructs the simulator on how to test the chip.
3. **`.cmp` (Compare File):** Contains the correct expected outputs.

**To Test:** Load the `.hdl` and `.tst` files into the simulator and run the script. The simulator will report an error if your actual outputs disagree with the desired outputs in the `.cmp` file.

---
*Reference: Based on the Nand to Tetris curriculum by Noam Nisan and Shimon Schocken.*
