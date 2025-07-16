#### **Sign Magnitude Representation**
- The **most significant bit (MSB)** is used as a **sign bit**:
    - `0` = Positive
    - `1` = Negative
- The remaining bits represent the magnitude of the number.

**Example:**
- `010101101` → **+173** (Sign bit = 0, value = 10101101 → 173)
- `110101101` → **-173** (Sign bit = 1, value = 10101101 → 173)

✅ **Disadvantage**: Sign magnitude has two representations for zero (`00000000` and `10000000`), which makes arithmetic operations complex.

---
#### **Two’s Complement Representation**
- The **most significant bit (MSB)** represents a **negative** value (e.g., in 8-bit numbers, `MSB = -128` instead of `128`).
- Converting a negative number to two’s complement:
    1. **Invert all bits** (flip 0s to 1s and 1s to 0s).
    2. **Add 1** to the inverted result.

**Example: Convert `7` to `-7` using Two’s Complement (8-bit format)**

1. `00000111` → **Binary for `7`**
2. Flip all bits: `11111000`
3. Add `1`: `11111001`

**Verification (Decimal Conversion)**

`-128  64  32  16  8   4   2   1     1    1   1   1   1   0   0   1`  

`(-128 × 1) + (64 × 1) + (32 × 1) + (16 × 1) + (8 × 1) + (4 × 0) + (2 × 0) + (1 × 1) = -7` ✅

✅ **Advantage**: Only one representation for zero and simplifies binary arithmetic.