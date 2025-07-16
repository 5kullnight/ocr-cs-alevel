- **Processor**: Known as the computer's brain; executes instructions to run programs.

![[Pasted image 20241227173034.png]]
# 1. Control Unit (CU):
- Directs CPU operations and coordinates activities:
    - Controls CPU actions.
    - Manages data flow between CPU and other devices.
    - Accepts, decodes, and executes instructions.
    - Stores results back into memory.
- **Example:**
	- Imagine a busy restaurant. The **Control Unit** is like the **manager** of the restaurant, ensuring all staff (components of the CPU) perform their tasks efficiently and in the correct order.
---
# 2. Registers:
- **Definition**: Small, high-speed memory cells for temporary data storage.
- **Types of Registers**:
    - **Program Counter (PC)**: Holds the next instruction’s address.
    - **Accumulator (ACC)**: Stores calculation results.
    - **Memory Address Register (MAR)**: Holds addresses for reading/writing data.
    - **Memory Data Register (MDR)**: Temporarily stores data being read/written.
    - **Current Instruction Register (CIR)**: Holds the instruction being executed, split into:
        - **Operand**: Data/address to operate on.
        - **Opcode**: Specifies the operation type
### Step-by-Step Explanation of Register Usage:
#### 1. Program Counter (PC)
- **What it does**: Keeps track of the address of the next instruction.
- **Example**:
    - The program's first instruction, "Load 7 into ACC," (When you enter a number into a calculator, it shows up on the screen, ready for the next operation) is at memory address **0x01** (doesn't matter, its just how computer names instructions).
    - The **PC** starts at **0x01**.
    - After the instruction is executed, the PC increments to **0x02** to fetch the next instruction.
#### 2. Memory Address Register (MAR)
- **What it does**: Holds the memory address where data or instructions will be read from or written to.
- **Example**:
    - The CPU needs to fetch the first instruction from address **0x01**.
    - The **MAR** is set to **0x01**, pointing to the memory location holding "Load 7 into ACC."
#### 3. Memory Data Register (MDR)
- **What it does**: Temporarily holds data read from memory or data to be written into memory.
- **Example**:
    - The CPU fetches the instruction "Load 7 into ACC" from memory address **0x01**.
    - The **MDR** temporarily holds this instruction: "Load 7 into ACC."
#### 4. Current Instruction Register (CIR)
- **What it does**: Holds the current instruction being executed.
- **Example**:
    - After fetching, the instruction "Load 7 into ACC" is copied into the **CIR**.
    - The CPU now decodes and executes it:
        - **Opcode**: "Load" (what operation to perform).
        - **Operand**: "7" (data to load).
#### 5. Accumulator (ACC)
- **What it does**: used to temporarily store the results of the calculations or operations. All input/output data passes through the accumulator e.g. like a buffer (e.g., IN loads data into it; OUT sends its value to the screen)
- **Example**:
    - After decoding the instruction "Load 7 into ACC," the CPU stores **7** in the **ACC**.
    - Next, the instruction "Add 5 to ACC" is fetched and executed.
    - The **ACC** updates to **12** after the addition.
#### Example Flow Summary
1. **PC** starts at **0x01**.
2. **MAR** points to **0x01**.
3. **MDR** fetches "Load 7 into ACC" from memory.
4. **CIR** decodes "Load 7 into ACC."
5. **ACC** stores **7**.
6. **PC** increments to **0x02** for the next instruction ("Add 5 to ACC").
7. **MAR**, **MDR**, **CIR**, and **ACC** repeat the cycle to add **5**, resulting in **12**.
### Visualizing the Process
 
| Register | Role                     | Example Value     |
| -------- | ------------------------ | ----------------- |
| **PC**   | Next instruction address | 0x01, then 0x02   |
| **MAR**  | Memory address to access | 0x01              |
| **MDR**  | Data fetched or to write | "Load 7 into ACC" |
| **CIR**  | Current instruction      | "Load 7 into ACC" |
| **ACC**  | Operation result         | 7 → 12            |

---
# 3. Arithmetic and Logic Unit (ALU):
- Performs **arithmetic operations**: e.g., addition, subtraction (on fixed/floating point numbers).
- Performs **logical operations**: Boolean logic like AND, OR, NOT, XOR.
#### Example: Addition Instruction
1. **Operation**: Add two numbers.
2. **Input**: Two binary numbers.
    - Example: `5` (binary: `0101`) and `3` (binary: `0011`).
3. **ALU Action**: Perform binary addition.
    - `0101 + 0011 = 1000` (binary), which equals `8` in decimal.
4. **Output**: The result of the addition (`1000`).
---
# 4. Buses in the CPU:
- **Definition**: Parallel wires connecting CPU components; grouped as the **system bus**.
- **Bus Width**: Number of wires; determines bits transferable at once (e.g., 8, 16, 32, 64 bits).
	  - 8 bit Gaming Consoles: Nintendo Entertainment System (NES).
	  - 16 bit Gaming Consoles: Super Nintendo Entertainment System (SNES). Sega Genesis.
	  - 32 bit Gaming Consoles: Nintendo 64 (despite its name, much of the system's data paths were 32-bit); Operating Systems: Windows XP and earlier 32-bit OS versions.
	  - 64 bit Modern Computers: All modern desktops and laptops; Gaming Consoles: PlayStation 4, Xbox One, and later consoles.
- **Example:**
	- Buses in a CPU are like **highways** that allow information to travel between different parts of the computer. There are three main types of buses, each serving a specific purpose: **Data Bus**, **Address Bus**, and **Control Bus**.
#### Types of Buses:
1. **Data Bus**:
	- **Purpose**: Transfers actual data (operands, instructions, or memory addresses) between the CPU (registers, ALU, control unit), RAM (main memory) and I/O devices (in some architectures)
	- **Direction**: **Bi-directional** (data can flow both ways).
	- **In a CPU Example**:
		- Suppose the CPU needs to add two numbers stored in memory:
	    1. The CPU uses the **data bus** to fetch the numbers (e.g., **7** and **5**) from memory.
	    2. After the addition, the CPU uses the **data bus** again to send the result (e.g., **12**) back to memory.
2. **Address Bus**: 
	- **Purpose**: Transmits the memory addresses being sent from CPU to RAM.
	- **Direction**: **Uni-directional** (from CPU to memory or I/O devices).
	- **In a CPU Example**:
		- Continuing the example of adding two numbers:
	    1. The CPU uses the **address bus** to point to the memory location where the first number (**7**) is stored.
	    2. The address bus then points to the memory location of the second number (**5**) for retrieval.
3. **Control Bus**: 
    - **Purpose**: Sends control signals to manage how the CPU and other components communicate e.g. read or write
	- **Direction**: **Bi-directional** (coordinates signals both ways).
	- **In a CPU Example**:
		- While adding two numbers:
	    1. The control bus sends a **"read" signal** to memory, instructing it to send the number **7** to the CPU.
	    2. After the CPU processes the addition, the control bus sends a **"write" signal**, telling memory to store the result (**12**).
---
# 5. Pipelining:
- **Definition**: Simultaneous processing of multiple instructions by overlapping steps:
    1. Fetching one instruction.
    2. Decoding another.
    3. Executing a third.
#### **Analogy for Pipelining: Assembly Line in a Factory**
Imagine a factory making cars. Each car goes through multiple stages (steps) to be fully assembled:
1. **Stage 1**: Install the engine.
2. **Stage 2**: Attach the doors.
3. **Stage 3**: Paint the car.
4. **Stage 4**: Final inspection.
#### **Non-Pipelined Process (One-at-a-Time)**
- Each car goes through **all stages** before starting the next car.
- Result: Only **one car** is completed at a time.
- Efficiency: Slow, as workers at some stages wait for the previous car to finish.
#### **Stages in Pipelining for a Webpage**
1. **Fetch**: The CPU retrieves the instructions (e.g., "Download HTML, CSS, images") from memory.
2. **Decode**: The CPU decodes each instruction to determine what it needs to do (e.g., "Parse HTML structure").
3. **Execute**: The CPU executes the instruction (e.g., "Render a section of the page").
4. **Write Back**: The CPU stores results or sends them to other components (e.g., "Display rendered content on the screen").

- **Purpose**: Reduces CPU idle time, improves efficiency.
- **Types of Pipelining**:
    - **Instruction Pipelining**: Divides instruction processing into fetch, decode, execute.
    - **Arithmetic Pipelining**: Overlaps arithmetic operation steps.
---

