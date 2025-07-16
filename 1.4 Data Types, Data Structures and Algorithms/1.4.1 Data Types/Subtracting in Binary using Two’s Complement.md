Two’s complement makes binary subtraction easy because **subtracting a number is the same as adding its negative counterpart**.

#### **Example: Subtract `12` from `8` (`8 - 12`)**
1. **Convert 8 to binary (5-bit representation)**
    - `8` in binary (5 bits) → `01000`
2. **Convert 12 to two’s complement (5-bit representation)**
    - `12` in binary: `01100`
    - Flip all bits: `10011`
    - Add `1`: `10100` → **`-12` in two’s complement**
3. **Perform Binary Addition**
      `0 1 0 0 0   (8 in binary) + 1 0 1 0 0   (-12 in two’s complement) -----------------   1 1 1 0 0   (-4 in two’s complement)`
4. **Verify the Result (`11100`)**
    - This is a **negative number** because the **MSB is `1`**.
    - Convert `11100` back to decimal:
        - Flip bits: `00011`
        - Add `1`: `00100` (which is `4`)
        - Add the negative sign: **`-4`** ✅