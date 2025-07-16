In digital logic, understanding basic circuits is essential for designing and analyzing systems. Here are three fundamental circuits you need to know: **D-Type Flip Flops, Half Adders,** and **Full Adders**.

---
### **D-Type Flip Flops**
A **D-Type Flip Flop** is a basic memory element that can store a single bit of data. It has two main inputs:

- **D**: Data input
- **CLK**: Clock input (control signal)

The output of a D-type flip flop, denoted as **Q**, changes only at the rising edge of the clock pulse, meaning it captures the value of **D** when the clock transitions from low to high.

#### **Logic Circuit**
The D-type flip flop consists of four NAND gates arranged in a specific configuration. When the clock (CLK) ticks, the output **Q** is updated to reflect the value of **D**.

- **Key Points**:
    - It serves as a basic unit of memory.
    - Multiple flip-flops can be combined to create registers.

---
### **Adders**

Adders are logic circuits designed to perform binary addition. There are two types of adders: **Half Adders** and **Full Adders**.

---
### **Half Adder**
A **Half Adder** adds two single bits and produces two outputs: **Sum** (S) and **Carry** (C). It is composed of:
- **XOR Gate**: Produces the Sum
- **AND Gate**: Produces the Carry

#### **Truth Table for Half Adder**

|A|B|C (Carry)|S (Sum)|
|---|---|---|---|
|0|0|0|0|
|0|1|0|1|
|1|0|0|1|
|1|1|1|0|

- **Key Points**:
    - Produces a Sum when one input is true.
    - Produces a Carry when both inputs are true.

---
### **Full Adder**
A **Full Adder** extends the functionality of a half adder by including an additional input, **Cin** (Carry input), allowing it to add three bits. It consists of:
- **Two XOR Gates**: Calculate the Sum
- **Two AND Gates**: Calculate Carry values
- **One OR Gate**: Combines the Carry outputs

#### **Truth Table for Full Adder**

|A|B|Cin|Cout (Carry Out)|Sum|
|---|---|---|---|---|
|0|0|0|0|0|
|0|0|1|0|1|
|0|1|0|0|1|
|0|1|1|1|0|
|1|0|0|0|1|
|1|0|1|1|0|
|1|1|0|1|0|
|1|1|1|1|1|

- **Key Points**:
    - Can handle carries from previous additions, making it possible to chain multiple full adders together to create a **ripple adder**.
    - Inputs **B** and **Cin** can be connected to the previous adder's **S** and **Cout**, allowing for cascading additions.