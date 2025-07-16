Bitwise operations allow you to manipulate individual bits in binary numbers efficiently. They are widely used in low-level programming, cryptography, and data compression.

---
### **📌 1. Logical Shifts**
Logical shifts move all bits left or right, filling empty spaces with **zeros**.
#### **🔹 Logical Shift Left (LSL)**

Each left shift **doubles** the number (`×2 per shift`).

Example: Shift `10010110` left by **3** places.

`10010110  →  10010110000  (Shift left by 3)`

- Equivalent to multiplying by 23=82^3 = 823=8.

#### **🔹 Logical Shift Right (LSR)**

Each right shift **halves** the number (`÷2 per shift`).

Example: Shift `10010110` right by **2** places.

`10010110  →  00100101  (Shift right by 2)`

- Equivalent to dividing by 22=42^2 = 422=4 (integer division).

---

### **📌 2. Bit Masks**

A **bitmask** is a binary number used to extract, modify, or check specific bits in another number using **bitwise operations**.

#### **🔹 AND Mask (`&`)**

- **Used to extract bits**.
- Only bits that are `1` in **both** numbers remain `1`, otherwise `0`.

Example:

  `00101011 & 10111011 ------------   00101011`

✅ **Use case:** Checking if a bit is set (`1`).

#### **🔹 OR Mask (`|`)**

- **Used to set bits**.
- Any `1` in **either** number results in `1`.

Example:

  `00101011 | 10111011 ------------   10111011`

✅ **Use case:** Turning on specific bits.

#### **🔹 XOR Mask (`^`)**

- **Used to toggle bits**.
- Bits that are different become `1`, bits that are the same become `0`.

Example:

  `00101011 ^ 10111011 ------------   10010000`

✅ **Use case:** Flipping bits.