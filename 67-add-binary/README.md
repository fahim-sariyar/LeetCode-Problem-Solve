# 67. Add Binary (Easy)

## 📝 Problem Description

Given two binary strings `a` and `b`, return their sum as a binary string.

### Example 1:
Input:
a = "11"  
b = "1"  

Output:
"100"

### Example 2:
Input:
a = "1010"  
b = "1011"  

Output:
"10101"

### Constraints:
- 1 <= a.length, b.length <= 10^4
- `a` and `b` consist only of '0' or '1'
- No leading zeros except "0"

---

## 💡 Approach

We simulate binary addition just like manual addition:

- Start from the last index of both strings.
- Add digits along with carry.
- Store result.
- Reverse the final string.

Time Complexity: **O(n)**  
Space Complexity: **O(n)**  

---
