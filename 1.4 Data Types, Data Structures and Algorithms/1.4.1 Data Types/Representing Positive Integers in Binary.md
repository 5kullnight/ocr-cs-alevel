# Binary Basics
- Computers use **base 2 (binary)**, whereas humans use **base 10 (decimal)**.
- **Bit:** A single binary digit (0 or 1).
- **Byte:** 8 bits.
- **Nybble:** 4 bits (half a byte).

# Binary to Decimal Conversion
- Each **bit’s place value** is a power of 2 (starting from 202^020 on the right).
- Example:  
    **1101 in binary → decimal** (1×8)+(1×4)+(0×2)+(1×1)=13(1 \times 8) + (1 \times 4) + (0 \times 2) + (1 \times 1) = 13(1×8)+(1×4)+(0×2)+(1×1)=13 **1101 (binary) = 13 (decimal)**

# Decimal to Binary Conversion
1. **Find the largest power of 2** smaller than the number.
2. **Write out place values** in descending order (e.g., 32, 16, 8, 4, 2, 1).
3. **Determine 1s and 0s** by checking if the place value fits into the number.
4. **Subtract and continue** with the remainder.

Example: Convert **47 (decimal) to binary**

- Largest power of 2 ≤ 47: **32** → Write **1**, subtract 32 → **15** remains.
- Next power **16** > 15 → Write **0**.
- **8** ≤ 15 → Write **1**, subtract **8** → **7** remains.
- **4** ≤ 7 → Write **1**, subtract **4** → **3** remains.
- **2** ≤ 3 → Write **1**, subtract **2** → **1** remains.
- **1** ≤ 1 → Write **1**, subtract **1** → **0** remains.

**Binary representation of 47: `101111`**
- Represented as a **byte**: **`00101111`** (adding leading zeros).