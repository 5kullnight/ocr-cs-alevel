- **Definition**: Small, high-speed memory cells for temporary data storage.
- **Types of Registers**:
    - **Program Counter (PC)**: Holds the next instruction’s address.
    - **Accumulator (ACC)**: Stores calculation results.
    - **Memory Address Register (MAR)**: Holds addresses for reading/writing data.
    - **Memory Data Register (MDR)**: Temporarily stores data being read/written.
    - **Current Instruction Register (CIR)**: Holds the instruction being executed, split into:
        - **Operand**: Data/address to operate on.
        - **Opcode**: Specifies the operation type.

# Step-by-Step Explanation of Register Usage
#### 1. **Program Counter (PC)**
- **What it does**: Keeps track of the address of the next instruction.
- **Example**:
    - The program's first instruction, "Load 7 into ACC," (When you enter a number into a calculator, it shows up on the screen, ready for the next operation) is at memory address **0x01** (doesn't matter, its just how computer names instructions).
    - The **PC** starts at **0x01**.
    - After the instruction is executed, the PC increments to **0x02** to fetch the next instruction.

---
#### 2. **Memory Address Register (MAR)**
- **What it does**: Holds the memory address where data or instructions will be read from or written to.
- **Example**:
    - The CPU needs to fetch the first instruction from address **0x01**.
    - The **MAR** is set to **0x01**, pointing to the memory location holding "Load 7 into ACC."

---
#### 3. **Memory Data Register (MDR)**
- **What it does**: Temporarily holds data read from memory or data to be written into memory.
- **Example**:
    - The CPU fetches the instruction "Load 7 into ACC" from memory address **0x01**.
    - The **MDR** temporarily holds this instruction: "Load 7 into ACC."

---
#### 4. **Current Instruction Register (CIR)**
- **What it does**: Holds the current instruction being executed.
- **Example**:
    - After fetching, the instruction "Load 7 into ACC" is copied into the **CIR**.
    - The CPU now decodes and executes it:
        - **Opcode**: "Load" (what operation to perform).
        - **Operand**: "7" (data to load).

---
#### 5. **Accumulator (ACC)**
- **What it does**: Stores the results of calculations or operations.
- **Example**:
    - After decoding the instruction "Load 7 into ACC," the CPU stores **7** in the **ACC**.
    - Next, the instruction "Add 5 to ACC" is fetched and executed.
    - The **ACC** updates to **12** after the addition.

---
### Example Flow Summary
1. **PC** starts at **0x01**.
2. **MAR** points to **0x01**.
3. **MDR** fetches "Load 7 into ACC" from memory.
4. **CIR** decodes "Load 7 into ACC."
5. **ACC** stores **7**.
6. **PC** increments to **0x02** for the next instruction ("Add 5 to ACC").
7. **MAR**, **MDR**, **CIR**, and **ACC** repeat the cycle to add **5**, resulting in **12**.
---
### Visualizing the Process

| Register | Role                     | Example Value     |
| -------- | ------------------------ | ----------------- |
| **PC**   | Next instruction address | 0x01, then 0x02   |
| **MAR**  | Memory address to access | 0x01              |
| **MDR**  | Data fetched or to write | "Load 7 into ACC" |
| **CIR**  | Current instruction      | "Load 7 into ACC" |
| **ACC**  | Operation result         | 7 → 12            |
