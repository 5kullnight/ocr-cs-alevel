### **Overview of Boolean Logic**
Boolean logic uses binary values (True or False, represented as 1 or 0) to define problems and perform operations. There are four fundamental operations in Boolean logic:
- **Conjunction (AND)**
- **Disjunction (OR)**
- **Negation (NOT)**
- **Exclusive Disjunction (XOR)**

---
### **Logic Gates and Their Symbols**

|Operation|Logic Gate|Symbol|
|---|---|---|
|Conjunction (AND)|AND|⋅|
|Disjunction (OR)|OR|+|
|Negation (NOT)|NOT|¬|
|Exclusive Disjunction (XOR)|XOR|⊕|

---
### **Truth Tables**
A **truth table** displays every possible input combination for a logic gate and the corresponding output. Inputs are typically labeled A, B, C, etc.

---
### **1. Conjunction (AND)**
- **Definition:** The AND gate produces an output of True (1) only when both inputs are True (1). It can be thought of as multiplying its binary inputs.
#### **Truth Table for AND Gate**

|A|B|A ⋅ B|
|---|---|---|
|0|0|0|
|0|1|0|
|1|0|0|
|1|1|1|

---
### **2. Disjunction (OR)**
- **Definition:** The OR gate produces an output of True (1) if at least one of the inputs is True (1). It can be thought of as adding its inputs.
#### **Truth Table for OR Gate**

|A|B|A + B|
|---|---|---|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

---
### **3. Negation (NOT)**
- **Definition:** The NOT gate takes a single input and reverses its truth value. For example, NOT 1 is 0, and NOT 0 is 1.
#### **Truth Table for NOT Gate**

|A|¬A|
|---|---|
|0|1|
|1|0|

---
### **4. Exclusive Disjunction (XOR)**
- **Definition:** The XOR gate produces an output of True (1) only when exactly one of the inputs is True (1). If both inputs are True, the output is False (0).
#### **Truth Table for XOR Gate**

|A|B|A ⊕ B|
|---|---|---|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|