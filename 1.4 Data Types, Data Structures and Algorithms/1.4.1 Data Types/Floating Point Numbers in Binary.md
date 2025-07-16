Floating point numbers in binary are similar to scientific notation in decimal. They are used to represent very large or very small numbers while maintaining precision.

---
### **Components of Floating Point Representation**
A floating point number consists of three parts:
1. **Sign (S)** – 1 bit
    - `0` → Positive number
    - `1` → Negative number
2. **Mantissa (M)** – Represents the significant digits of the number
    - The binary point (equivalent to the decimal point) is placed **after the first 1** in the mantissa.
    - The mantissa is normalized (starts with `1.xxxxx`).
3. **Exponent (E)** – Specifies how many places to shift the binary point
    - Stored in **two’s complement** format
    - A **positive exponent** moves the binary point **right** (making the number larger).
    - A **negative exponent** moves the binary point **left** (making the number smaller).

---
### **Example 1: Convert a Floating-Point Number to Decimal**
#### Given Floating Point Representation:

`S  M (10-bit)       E (6-bit) 0  1 1 0 0 1 0 0 1 1  1 0 0 0 1 0 1`
#### **Step 1: Identify Components**
- **Sign bit:** `0` → Positive number
- **Mantissa:** `1.100100111`
- **Exponent:** `100101` (Convert to decimal using **two’s complement**)

#### **Step 2: Convert Exponent to Decimal**
- `100101` (6-bit two’s complement)
- First bit (`1`) indicates it's negative. Find the two’s complement:
    `100101 → Invert bits → 011010 → Add 1 → 011011 = **Decimal 5**`
- So, **Exponent = 5**
#### **Step 3: Adjust the Binary Point**
- `1.100100111` → Move **5 places right** → `110010.0111`
#### **Step 4: Convert to Decimal**

`Binary:  110010.0111          32  16  0  4  2  1  0.5  0.25  0.125  0.0625          1   1   0  0  1  0   .    0    1     1     1`

(1×32)+(1×16)+(1×2)+(0.25)+(0.125)+(0.0625)=50.4375(1 \times 32) + (1 \times 16) + (1 \times 2) + (0.25) + (0.125) + (0.0625) = 50.4375(1×32)+(1×16)+(1×2)+(0.25)+(0.125)+(0.0625)=50.4375

✅ **Final Answer: `50.4375`**

---

### **Example 2: Convert Another Floating-Point Number to Decimal**
#### Given Floating Point Representation:

`S  M (10-bit)       E (6-bit) 1  0 1 0 1 1 0 1 0 0  0 1 1 1 1 0 1`

#### **Step 1: Identify Components**
- **Sign bit:** `1` → Negative number
- **Mantissa:** `0.101101000`
- **Exponent:** `011101` (Convert to decimal using **two’s complement**)

#### **Step 2: Convert Exponent to Decimal**
- `011101` (Positive in two’s complement)
- Convert to decimal: (0×−32)+(1×16)+(1×8)+(1×4)+(0×2)+(1×1)=16+8+4+1=∗∗−3∗∗(0 \times -32) + (1 \times 16) + (1 \times 8) + (1 \times 4) + (0 \times 2) + (1 \times 1) = 16 + 8 + 4 + 1 = **-3**(0×−32)+(1×16)+(1×8)+(1×4)+(0×2)+(1×1)=16+8+4+1=∗∗−3∗∗
- **Exponent = -3**

#### **Step 3: Adjust the Binary Point**
- `0.101101000` → Move **3 places left** → `0.000101101`
#### **Step 4: Convert to Decimal**

`Binary:  0.000101101            1/16   1/32   1/64   1/128   1/256             0       0      0      1       0       1       1       0       1`

(1×1/16)+(0×1/32)+(1×1/64)+(1×1/128)+(1×1/512)(1 \times 1/16) + (0 \times 1/32) + (1 \times 1/64) + (1 \times 1/128) + (1 \times 1/512)(1×1/16)+(0×1/32)+(1×1/64)+(1×1/128)+(1×1/512) =0.0625+0+0.015625+0.0078125+0.001953125= 0.0625 + 0 + 0.015625 + 0.0078125 + 0.001953125=0.0625+0+0.015625+0.0078125+0.001953125 =0.087890625= 0.087890625=0.087890625

✅ **Final Answer: `-0.08789` (Approximately)**