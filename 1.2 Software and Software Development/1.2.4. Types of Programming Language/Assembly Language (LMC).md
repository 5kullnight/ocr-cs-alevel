Assembly language is a low-level programming language that serves as an abstraction over machine code. It provides a way to write instructions using mnemonics, which are easier to understand and remember compared to binary machine code.
When executed, an **assembler** translates the assembly code into machine code specific to the processor.

---
### **Key Features of Assembly Language**
1. **Use of Mnemonics**:
    - Human-readable instructions like `ADD`, `SUB`, and `LDA` replace binary machine code.
    - Each mnemonic corresponds to a specific processor instruction.
2. **Processor-Specific**:
    - Assembly code is written for a specific CPU architecture.
    - It interacts directly with the CPU's **special-purpose registers**.
3. **Close to Hardware**:
    - Provides fine-grained control over hardware resources.
    - Commonly used in **embedded systems** and **low-level programming**.
4. **1-to-1 Correspondence**:
    - Typically, each assembly instruction translates to one machine code instruction.
---
### **Assembly Mnemonics**

|**Mnemonic**|**Instruction**|**Function**|
|---|---|---|
|**ADD**|Add|Adds the value at a given memory address to the value in the Accumulator.|
|**SUB**|Subtract|Subtracts the value at a given memory address from the Accumulator.|
|**STA**|Store|Stores the value in the Accumulator at a given memory address.|
|**LDA**|Load|Loads the value at a given memory address into the Accumulator.|
|**INP**|Input|Allows user input to be stored in the Accumulator.|
|**OUT**|Output|Prints the value currently held in the Accumulator.|
|**HLT**|Halt|Stops the program.|
|**DAT**|Data|Creates a labeled memory location for data storage.|
|**BRZ**|Branch if Zero|Branches to a given address if the Accumulator value is zero (conditional).|
|**BRP**|Branch if Positive|Branches to a given address if the Accumulator value is positive (conditional).|
|**BRA**|Branch Always|Branches to a given address unconditionally.|

---
### **Example Program: Modulus Calculation**
The following example calculates the remainder when **num1** is divided by **num2** using the Little Man Computer (LMC) model.
#### **Code Breakdown**
`INP         // Input first number`
`STA num1    // Store it at 'num1'`
`INP         // Input second number`
`STA num2    // Store it at 'num2'`
`LDA num1    // Load 'num1' into Accumulator`
`positive    STA num1    // Save result back to 'num1'`
`SUB num2    // Subtract 'num2' from 'num1'`
`BRP positive // Branch to 'positive' if result is positive`
`LDA num1    // Load the remainder (value of 'num1')`
`OUT         // Output the remainder`
`HLT         // Halt the program`
`num1 DAT    // Declare memory location for 'num1'`
`num2 DAT    // Declare memory location for 'num2'`
#### **Execution Flow**
1. **Input and Storage**:
    - User inputs two numbers: `num1` and `num2`.
2. **Repeated Subtraction**:
    - Subtract `num2` from `num1` repeatedly until the result is less than zero.
3. **Output Remainder**:
    - The final value in `num1` is the remainder, which is output.
4. **Halt**:
    - The program terminates.
---
### **Advantages of Assembly Language**
- **Efficient**: Directly manipulates hardware for maximum performance.
- **Precise Control**: Fine-tunes system operations, such as memory and CPU management.
- **Essential for Embedded Systems**: Enables interaction with specific hardware components.
### **Disadvantages**
- **Processor Dependence**: Code must be rewritten for different CPU architectures.
- **Complexity**: Harder to write, debug, and maintain compared to high-level languages.
- **Low Productivity**: More time-consuming due to detailed and verbose code.
---
### **Use Cases**
- **Embedded Systems**: Firmware for microcontrollers in devices like washing machines and thermostats.
- **Performance-Critical Applications**: Optimizing tasks in game engines or real-time systems.
- **Operating Systems**: Writing or tweaking kernel-level code.
- **Device Drivers**: Low-level communication with hardware components.