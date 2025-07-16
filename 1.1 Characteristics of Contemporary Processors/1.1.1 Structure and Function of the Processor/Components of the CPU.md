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

| Registers                          | Purpose                                                                                                                                                           |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Program Counter (PC)               | Stores the address of the next instruction to be fetched.                                                                                                         |
| Memory Address Register (MAR)      | Holds the memory address of the instruction to be accessed in memory, sent from PC. It sends these addresses to memory down the address bus.                      |
| Memory Data Register (MDR)         | Stores the data/instruction that has been accessed from memory. It sends/receives this data from the data bus.                                                    |
| Current Instruction Register (CIR) | Holds the current instruction being executed, split up into operand (data/address to operate on) and opcode (specifies the operation type) as assembly mnemonics. |
| Accumulator (ACC)                  | A general-purpose register that temporarily stores the result from calculations. Also used as a buffer for I/O in processor.                                      |

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
- **Definition**: process of completing the fetch-decode-execute cycles of 3 separate instructions simultaneously. Allows one instruction to be fetched as the previous one is being decoded and the one before is being executed, reducing the amount of the CPU which is kept idle. However, if just/branch instructions exist the code will not pipeline well.
- **Purpose**: Reduces CPU idle time, improves efficiency.
#### **Example of stages in pipelining for a webpage**
1. **Fetch**: The CPU retrieves the instructions (e.g., "Download HTML, CSS, images") from memory.
2. **Decode**: The CPU decodes each instruction to determine what it needs to do (e.g., "Parse HTML structure").
3. **Execute**: The CPU executes the instruction (e.g., "Render a section of the page").
4. **Write Back**: The CPU stores results or sends them to other components (e.g., "Display rendered content on the screen").

