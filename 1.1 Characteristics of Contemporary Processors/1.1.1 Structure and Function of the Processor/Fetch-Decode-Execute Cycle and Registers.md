The **Fetch-Decode-Execute Cycle** is the process the CPU follows to execute an instruction. Let's break down each phase with examples to make it easier to understand.

--- 
# 1. Fetch Phase:
The CPU retrieves the next instruction from memory. This involves the following steps:
1. **Copy the address from the PC to the MAR**:
    - The **Program Counter (PC)** holds the address of the next instruction.
    - The address is copied to the **Memory Address Register (MAR)** to locate the instruction in memory.
2. **Retrieve the instruction using the data bus**:
    - The instruction at the specified address is fetched from RAM.
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
# 2. Decode Phase:
The CPU splits up into two parts the fetched instruction:
1. **Operand**: The data or memory address to operate on (e.g., **5**).
2. **Opcode**: The operation to perform (e.g., **ADD**).
**CIR** transfers the decoded instruction to CU (Control Unit) to store.
- **Decode Example**:
	- From the fetched instruction **"Add 5 to ACC":**
	    - **Opcode**: **ADD** (tells the CPU to perform an addition).
	    - **Operand**: **5** (the number to add to the accumulator).
---
# 3. Execute Phase:
The CPU carries out the decoded instruction. This could involve calculations, moving data, or interacting with memory.
1. **For arithmetic/logic operations:**
	1. The operand is fetched (via MAR/MDR) and sent to the ALU.
	2. The Accumulator (ACC) stores the result.
2. For jump instructions:
	1. The CIR sends the jump address back to the PC, overriding the usual +1 increment.
3. For writing to memory:
	1. Data from the ACC is copied to the MDR.
	2. The MAR holds the target address, and the control bus triggers a write.
- **Execute Example**:
	- The **ADD 5** instruction is executed:
	    1. The **ACC (Accumulator)** retrieves its current value (e.g., **7**).
	    2. The value **5** is added to the **ACC**.
	    3. The result (**12**) is stored back in the **ACC**.
---
# Cycle in Action:

|**Phase**|**Register Used**|**Action**|**Example**|
|---|---|---|---|
|**Fetch**|PC → MAR → MDR → CIR|Fetch instruction from memory|Fetch "Add 5 to ACC" from **0x01**.|
|**Decode**|CIR|Split into opcode and operand|Decode: Opcode = ADD, Operand = 5.|
|**Execute**|ACC|Perform the operation (e.g., ADD)|Add 5 to ACC (7 → 12).|
