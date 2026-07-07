# Project 1: Elementary Logic Gates

## Overview
This repository contains the implementations for a typical set of elementary logic gates. These gates form the foundational building blocks required to construct a computer's CPU and RAM in subsequent projects. The architecture assumes a 16-bit machine.

## Objective
The objective of this project is to build the following logic gates (chips) using Hardware Description Language (HDL), starting from a primitive `Nand` gate:

### Basic Gates
* `Not`
* `And`
* `Or`
* `Xor`
* `Mux`
* `DMux`

### 16-bit Variants
* `Not16`
* `And16`
* `Or16`
* `Mux16`

### Multi-Way Variants
* `Or8Way`
* `Mux4Way16`
* `Mux8Way16`
* `DMux4Way`
* `DMux8Way`

## Implementation Details
* **Primitive:** The `Nand` gate is considered primitive, meaning it does not need to be implemented and is provided as a base.
* **HDL Files:** Each chip is implemented by completing the missing `PARTS` section within the provided skeletal `Xxx.hdl` stub files.
* **Design Principle:** While every chip can be implemented using only `Nand` gates, any previously built chip from this project can be used as a component to keep the design simple and minimize the number of chip-parts used. 

## Testing and Verification
The chip implementations are verified using the **Nand2Tetris Hardware Simulator** (either the desktop version or the Online IDE).

For every chip `Xxx`, the repository includes:
1.  **`Xxx.tst` (Test Script):** Tells the hardware simulator how to test the chip.
2.  **`Xxx.cmp` (Compare File):** Contains the correct expected outputs.

**To Test:**
Load the `.hdl` file and its corresponding `.tst` script into the simulator. The simulator will run the test and compare the generated outputs against the `.cmp` file, reporting any errors if the actual outputs disagree with the desired results.

---
*Reference: Based on the Nand to Tetris curriculum by Noam Nisan and Shimon Schocken.*
