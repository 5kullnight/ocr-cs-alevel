Hexadecimal is a number system with a **base of 16**, meaning it uses **16 unique symbols**:
- **0-9** represent values 0 to 9.
- **A-F** represent values 10 to 15.

|Decimal|Hexadecimal|
|---|---|
|0|0|
|1|1|
|2|2|
|3|3|
|4|4|
|5|5|
|6|6|
|7|7|
|8|8|
|9|9|
|10|A|
|11|B|
|12|C|
|13|D|
|14|E|
|15|F|

---
## **Converting Between Hexadecimal and Other Number Systems**

### **Hexadecimal to Decimal**
Each digit in a hexadecimal number represents a power of **16**.
#### **Example: Convert `4E7F` to Decimal**

`Hex:  4   E   7   F         4096  256  16  1  (Place values: 16^3, 16^2, 16^1, 16^0)`

Convert `E` and `F` to decimal:

- `E = 14`
- `F = 15`

Now, multiply by place values:

(4×4096)+(14×256)+(7×16)+(15×1)(4 \times 4096) + (14 \times 256) + (7 \times 16) + (15 \times 1)(4×4096)+(14×256)+(7×16)+(15×1) 16384+3584+112+15=2009516384 + 3584 + 112 + 15 = 2009516384+3584+112+15=20095

✅ **So, `4E7F` in decimal is `20095`.**

---
### **Hexadecimal to Binary**

Each **hex digit** can be converted into a **4-bit binary equivalent** (called a "nybble").

#### **Example: Convert `B2` to Binary**
1. Split into hexadecimal digits: `B` and `2`.
2. Convert each hex digit to decimal:
    - `B = 11`
    - `2 = 2`
3. Convert each decimal to binary (4-bit nybbles):
    - `B (11) → 1011`
    - `2 (2) → 0010`
4. Combine the nybbles:  
    ✅ `B2 (Hex) = 10110010 (Binary)`

---

### **Hexadecimal to Decimal Using Place Values**
Instead of converting to binary first, you can use place values directly.
#### **Example: Convert `4C3` to Decimal**
(4×256)+(C×16)+(3×1)(4 \times 256) + (C \times 16) + (3 \times 1)(4×256)+(C×16)+(3×1)

Since `C = 12` in decimal:

(4×256)+(12×16)+(3×1)(4 \times 256) + (12 \times 16) + (3 \times 1)(4×256)+(12×16)+(3×1) 1024+192+3=12191024 + 192 + 3 = 12191024+192+3=1219

✅ **So, `4C3` in decimal is `1219`.**

---
### **Quick Reference Table**

|Hex|Binary|Decimal|
|---|---|---|
|0|0000|0|
|1|0001|1|
|2|0010|2|
|3|0011|3|
|4|0100|4|
|5|0101|5|
|6|0110|6|
|7|0111|7|
|8|1000|8|
|9|1001|9|
|A|1010|10|
|B|1011|11|
|C|1100|12|
|D|1101|13|
|E|1110|14|
|F|1111|15|

This makes hexadecimal **useful for representing binary numbers in a compact way** (since each hex digit represents 4 bits).