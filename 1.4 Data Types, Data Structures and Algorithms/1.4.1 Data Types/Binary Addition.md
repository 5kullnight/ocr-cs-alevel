#### **Binary Addition Rules**
1. **0 + 0 = 0**
2. **0 + 1 = 1**
3. **1 + 1 = 10** (write 0, carry 1)
4. **1 + 1 + 1 = 11** (write 1, carry 1)

#### **Example: Add `1011` and `1110`**

   `1011 + 1110 ------   11001`

**Step-by-step explanation:**
- **Rightmost column:** 1 + 0 = 1
- **Next column:** 1 + 1 = 10 → Write **0**, carry **1**
- **Next column:** 0 + 1 + (carried 1) = 10 → Write **0**, carry **1**
- **Leftmost column:** 1 + 1 + (carried 1) = 11 → Write **1**, carry **1**
- **Final carry:** Write **1** at the front
Final result: **11001 (binary)**

#### **Checking the Answer (Convert to Decimal)**
- `1011` (binary) = **11 (decimal)**
- `1110` (binary) = **14 (decimal)**
- **11 + 14 = 25**
- `11001` (binary) = **25 (decimal) ✅**