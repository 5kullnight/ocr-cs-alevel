#### **Reduced Instruction Set Computers (RISC)**
- **Characteristics**:
    - Uses a **small instruction set**.
    - Each instruction takes **one clock cycle** to execute.
    - Instructions are simple and written as **single lines of machine code**.
- **Example** (Multiply two numbers XXX and YYY):
    `LDA R1, X   ; Load X into register R1   LDA R2, Y   ; Load Y into register R2   MULT R1, R2 ; Multiply contents of R1 and R2   STO R1, X   ; Store result in X`  
- **Advantages**:
    - **Pipelining is efficient** because all instructions are uniform in execution time.
    - Ideal for performance-critical tasks like gaming or multimedia applications.
- **Disadvantage**:
    - Requires **more RAM** since code is longer.
#### **Complex Instruction Set Computers (CISC)**
- **Characteristics**:
    - Uses a **large instruction set**.
    - Each instruction can accomplish **complex tasks** in fewer lines of code.
    - Many instructions are built into the hardware, even if they’re rarely used.
- **Example** (Same task as above):
    `MULT A, B ; Multiply A and B and store result`  
- **Advantages**:
    - **Shorter code**, so less RAM is required.
    - The **compiler has less work** to translate high-level code into machine code.
- **Disadvantage**:
    - **Pipelining is less efficient** since instructions vary in execution time.
#### Modern processors often mix characteristics:
- **CISC Processors** (e.g., x86) use **RISC-like microoperations** internally to improve efficiency.
- **RISC Processors** (e.g., ARM) include more complex instructions for specific tasks to reduce software overhead.
#### **1. Intel and AMD Processors (x86 Architecture)**
- **Processor Examples**:
    - Intel Core i9, AMD Ryzen 9.
- **CISC by Design, RISC-Like Internally**:
    - x86 processors use a **CISC instruction set**, which includes complex instructions.
    - Internally, these instructions are broken down into smaller, simpler **micro-operations (µops)**, resembling RISC-style instructions.
    - The use of **out-of-order execution** and **pipelining** is heavily influenced by RISC principles to improve efficiency.
---
#### **2. Apple M-Series Processors (M1, M2)**
- **RISC at its Core with Advanced Features**:
    - These ARM-based processors are RISC by design but integrate features that allow them to execute certain tasks in fewer steps, bridging some complexity seen in CISC.
    - **Unified Memory Architecture (UMA)** and advanced optimizations blur the RISC-CISC divide.
#### In summary:
- **RISC**: Dominates mobile and low-power applications.
- **CISC**: Still strong in general-purpose computing and high-performance systems.
### **Comparison Table*

| **Aspect**            | **RISC Processors**             | **CISC Processors**        |
| --------------------- | ------------------------------- | -------------------------- |
| **Instruction Set**   | Small, simple                   | Large, complex             |
| **Execution Time**    | One clock cycle per instruction | Varies by instruction      |
| **Code Length**       | Longer (more lines)             | Shorter                    |
| **RAM Requirement**   | More (stores longer code)       | Less (stores compact code) |
| **Compiler Workload** | High (simplifies complex tasks) | Low                        |
| **Pipelining**        | Highly efficient                | Less efficient             |

### **How to Remember**
- **RISC**: **"Reduced and Repeated"** – Fewer instructions, executed fast, but takes more memory.
- **CISC**: **"Complex and Compact"** – Handles complex tasks in fewer lines but slower execution overall.