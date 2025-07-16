**Normalisation** ensures that floating point numbers are as precise as possible by adjusting the mantissa to make full use of its bits. The goal is to adjust the binary number so that:
- **Positive numbers** start with `01`
- **Negative numbers** start with `10`

This ensures that floating point numbers have a **consistent representation** and avoid unnecessary leading zeros.

---
### **Example: Normalise `000110100101`**
We are given a **12-bit** floating point number:
`000110100101`
- **Mantissa (8 bits):** `00011010`
- **Exponent (4 bits):** `0101`
#### **Step 1: Adjust the Mantissa**
Since the number is **positive**, we must shift the mantissa until it starts with `01`.  
Current mantissa: `00011010`
- Shift **2 places left** → `01101000`
- Fill the empty spaces with `0`s.
#### **Step 2: Adjust the Exponent**
Since we shifted **2 places left**, we **decrease** the exponent by **2**.
- Current exponent: `5₁₀` (`0101` in binary)
- New exponent: `5 - 2 = 3₁₀` (`0011` in binary)

#### **Final Normalised Representation**
`0 1 1 0 1 0 0 0  0 0 1 1 Mantissa          Exponent`

This is the **correct normalised form** of the floating point number! ✅

---

### **Key Takeaways**
1. **Normalisation shifts the mantissa** so that it starts with `01` (for positive numbers) or `10` (for negative numbers).
2. **The exponent is adjusted accordingly** to ensure the number's value remains the same.
3. **Normalisation maximises precision**, ensuring that the most significant bits are always used effectively.