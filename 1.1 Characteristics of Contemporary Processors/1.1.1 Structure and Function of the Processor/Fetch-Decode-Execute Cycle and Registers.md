The **Fetch-Decode-Execute Cycle** is the process the CPU follows to execute an instruction. Let's break down each phase with examples to make it easier to understand.

--- 
### **1. Fetch Phase**
The CPU retrieves the next instruction from memory. This involves the following steps:
1. **Copy the address from the PC to the MAR**:
    - The **Program Counter (PC)** holds the address of the next instruction.
    - The address is copied to the **Memory Address Register (MAR)** to locate the instruction in memory.
2. **Retrieve the instruction using the data bus**:
    - The instruction at the specified address is fetched from memory.
    - It is temporarily stored in the **Memory Data Register (MDR)**.
3. **Increment the PC**:
    - The **Program Counter (PC)** increments by 1 to point to the address of the next instruction.
4. **Copy the instruction to the CIR**:
    - The fetched instruction in the MDR is copied into the **Current Instruction Register (CIR)** for decoding.
- **Fetch Example**:
	- Suppose the CPU is processing the program instruction **"Add 5 to ACC."**
	1. The **PC** points to memory address **0x01**, where this instruction is stored.
	2. **MAR** holds **0x01**, and the instruction is fetched into the **MDR**: **"Add 5 to ACC."**
	3. **PC** increments to **0x02** to fetch the next instruction.
	4. The fetched instruction is copied to the **CIR**.
---
### **2. Decode Phase**
The CPU interprets the fetched instruction by splitting it into two parts:
1. **Operand**: The data or memory address to operate on (e.g., **5**).
2. **Opcode**: The operation to perform (e.g., **ADD**).
- **Decode Example**:
	- From the fetched instruction **"Add 5 to ACC":**
	    - **Opcode**: **ADD** (tells the CPU to perform an addition).
	    - **Operand**: **5** (the number to add to the accumulator).
---
### **3. Execute Phase**
The CPU carries out the decoded instruction. This could involve calculations, moving data, or interacting with memory.
- **Execute Example**:
	- The **ADD 5** instruction is executed:
	    1. The **ACC (Accumulator)** retrieves its current value (e.g., **7**).
	    2. The value **5** is added to the **ACC**.
	    3. The result (**12**) is stored back in the **ACC**.
---
### **Cycle in Action**:

|**Phase**|**Register Used**|**Action**|**Example**|
|---|---|---|---|
|**Fetch**|PC → MAR → MDR → CIR|Fetch instruction from memory|Fetch "Add 5 to ACC" from **0x01**.|
|**Decode**|CIR|Split into opcode and operand|Decode: Opcode = ADD, Operand = 5.|
|**Execute**|ACC|Perform the operation (e.g., ADD)|Add 5 to ACC (7 → 12).|
### **Analogy: Following a Recipe**
Imagine you are a chef preparing a dish using a recipe. Each step of the recipe is like an instruction the CPU processes.

---
### **1. Fetch Phase (Getting the Recipe Step)**
- You (chef) open the recipe book to find the next step of the recipe.
- You copy that step into your memory to work on it.
**Steps in CPU Terms:**
1. **Program Counter (PC)**: Points to the step you’re currently on.
2. **Memory Address Register (MAR)**: Keeps track of where that step is in the book.
3. **Memory Data Register (MDR)**: Temporarily stores the instruction (e.g., "Chop 3 onions").
4. **Current Instruction Register (CIR)**: Copies the step so you can focus on it.
**Analogy Example**:
- You fetch the step **“Chop 3 onions”** from the recipe and prepare to follow it.
---
### **2. Decode Phase (Understanding the Step)**
- You read the fetched step to figure out what it means.
- Split the instruction into:
    - **Action (Opcode)**: What you need to do (e.g., chop).
    - **Data (Operand)**: What you need to act on (e.g., 3 onions).
**Analogy Example**:
- You read the instruction:
    - **Action**: Chop.
    - **Data**: 3 onions.
---
### **3. Execute Phase (Perform the Action)**
- You perform the action specified in the step.
**CPU Example**:
- If the instruction is **ADD 5 to ACC**, the CPU adds 5 to the accumulator.
**Analogy Example**:
- You take your knife and chop 3 onions.
---
### **Putting it Together in the Kitchen**
1. **Fetch**: Find the next step in the recipe (**“Chop 3 onions”**).
2. **Decode**: Understand what to do (**Chop**) and with what (**3 onions**).
3. **Execute**: Perform the action (chop the onions).