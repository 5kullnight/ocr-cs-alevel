When performing **addition and subtraction** with floating point numbers, the key steps are:

1. **Align the exponents** (make them the same by shifting the mantissa).
2. **Perform binary addition or subtraction** on the mantissas.
3. **Normalize the result** to ensure precision.

---

### **📌 Floating Point Addition Example**
Given two floating point numbers with:
- **Sign bit (1 bit)**
- **Mantissa (6 bits)**
- **Exponent (4 bits)**

`0 000100 0011   (First number) 0 000101 0010   (Second number)`
#### **Step 1: Align the Exponents**
- The first number has **exponent = 3₁₀** (`0011` in binary).
- The second number has **exponent = 2₁₀** (`0010` in binary).
To align exponents, we shift the mantissa of the **second number** right by **one place**, increasing its exponent to match the first (`3`).

`0 001000 0010   (Shifted first number) 0 000101 0010   (Shifted second number)`

#### **Step 2: Add the Mantissas**
  `0 0 1 0 0 0  (First mantissa) + 0 0 0 1 0 1  (Second mantissa) ----------------   0 0 1 1 0 1  (Sum)`

Result after addition: `0 001101 0010`

#### **Step 3: Normalisation**
- The mantissa must start with `01` for a **positive number**.
- Shift the mantissa **one place left** → `011010`
- Decrease exponent by **one** → `0001`

✅ **Final Answer:** `0 011010 0001`

---

### **📌 Floating Point Subtraction Example**
Just like integer subtraction in binary, we use **two’s complement**.
#### **Steps:**
1. **Align the exponents** (same as addition).
2. **Convert the mantissa of the second number to two’s complement**:
    - Flip the bits.
    - Add 1.
3. **Perform binary addition**.
4. **Normalize the result**.