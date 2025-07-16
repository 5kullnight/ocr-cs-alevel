## **Combining Boolean Operations**
### **Overview**
Boolean equations can be constructed by combining various Boolean operators, similar to how mathematical operators are used. This allows for the description of complex relationships between variables (A, B, C, etc.) using logical operations. By creating a truth table for a given Boolean equation, we can analyze and simplify it using different techniques.

---
### **Creating a Truth Table**
Let's consider a Boolean expression involving variables A, B, and C. The truth table might look like this:

|A|B|C|Output Y|
|---|---|---|---|
|0|0|0|0|
|0|0|1|0|
|0|1|0|0|
|0|1|1|0|
|1|0|0|1|
|1|0|1|1|
|1|1|0|1|
|1|1|1|0|

---
### **Manipulating Boolean Expressions**
Boolean expressions can often be simplified, resulting in shorter expressions that yield the same truth table. Simplifying these expressions is beneficial for clarity and efficiency.

---
### **Karnaugh Maps**
A **Karnaugh map (K-map)** is a tool used to simplify Boolean expressions visually. It represents the truth table in a grid format, allowing for easy identification of patterns and groupings.

#### **Steps to Create a K-map:**
1. **Fill in the K-map** based on the truth table.
2. **Highlight the 1s** in groups of sizes that are powers of 2 (1, 2, 4, etc.), including wraparound.

#### **Example K-map for 3 Variables (A, B, C)**

|AB\C|00|01|11|10|
|---|---|---|---|---|
|00|0|0|0|0|
|01|0|0|0|0|
|11|1|0|1|1|
|10|1|1|1|0|

---
### **Example Boolean Expression**
Given the Boolean expression: Y=(¬A∧(¬B∧¬C))∨(A∧(¬B∧C))∨(A∧(B∧¬C))∨(A∧¬(B∧¬C))Y = (\neg A \land (\neg B \land \neg C)) \lor (A \land (\neg B \land C)) \lor (A \land (B \land \neg C)) \lor (A \land \neg (B \land \neg C))Y=(¬A∧(¬B∧¬C))∨(A∧(¬B∧C))∨(A∧(B∧¬C))∨(A∧¬(B∧¬C))

#### **Truth Table for the Expression**

|A|B|C|Y|
|---|---|---|---|
|0|0|0|1|
|0|0|1|0|
|0|1|0|0|
|0|1|1|0|
|1|0|0|1|
|1|0|1|1|
|1|1|0|1|
|1|1|1|0|

#### **K-map for the Expression**

|AB\C|00|01|11|10|
|---|---|---|---|---|
|00|1|0|0|0|
|01|0|0|0|0|
|11|1|0|1|1|
|10|1|1|0|0|

---
### **Simplifying Using the K-map**
Once the K-map is filled out, highlight the groups of 1s as efficiently as possible:

1. **Vertical Rectangle:** Represents A∧¬BA \land \neg BA∧¬B (A is true, B is false; C can be either).
2. **Horizontal Rectangles:**
    - One rectangle indicates ¬B∧¬C\neg B \land \neg C¬B∧¬C (B and C are false).
    - The other indicates A∧¬CA \land \neg CA∧¬C (A is true, C is false; B can be either).

Combining these results, the simplified expression becomes: Y=(A∧¬B)∨(¬B∧¬C)∨(A∧¬C)Y = (A \land \neg B) \lor (\neg B \land \neg C) \lor (A \land \neg C)Y=(A∧¬B)∨(¬B∧¬C)∨(A∧¬C)