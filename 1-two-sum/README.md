# 1. Two Sum (Easy)

## 📝 Problem Description

Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.

- Each input has exactly one solution.
- You may not use the same element twice.
- You can return the answer in any order.

---

## 📌 Examples

### Example 1:
Input:
nums = [2,7,11,15], target = 9  
Output:
[0,1]  

Explanation:
nums[0] + nums[1] = 2 + 7 = 9  

---

### Example 2:
Input:
nums = [3,2,4], target = 6  
Output:
[1,2]

---

### Example 3:
Input:
nums = [3,3], target = 6  
Output:
[0,1]

---

## 🔒 Constraints

- 2 <= nums.length <= 10^4  
- -10^9 <= nums[i] <= 10^9  
- -10^9 <= target <= 10^9  

---

## 💡 Approach (Optimized - HashMap)

Instead of using two loops (O(n²)),  
we use a HashMap to store numbers and their indices.

### Steps:
1. Traverse the array.
2. For each element, calculate:
   complement = target - nums[i]
3. If complement exists in HashMap → return indices.
4. Otherwise store current element in HashMap.

Time Complexity: **O(n)**  
Space Complexity: **O(n)**  

---

## 💻 Java Solution

```java
import java.util.HashMap;

class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> map = new HashMap<>();
        
        for (int i = 0; i < nums.length; i++) {
            int complement = target - nums[i];
            
            if (map.containsKey(complement)) {
                return new int[] { map.get(complement), i };
            }
            
            map.put(nums[i], i);
        }
        
        return new int[] {};
    }
}
