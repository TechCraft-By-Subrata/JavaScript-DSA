## 🧩 Problem: "Longest Subarray With At Most K Distinct Elements"

### **Problem Description**

You are given an array of integers `nums` and an integer `k`.
Your task is to find the **length of the longest contiguous subarray** that contains **at most k distinct elements**.

Return the **length** of the longest such subarray.

---

### **Example 1**

**Input:**
```typescript
nums = [1, 2, 1, 2, 3]
k = 2
```
**Explanation:**
- The longest subarray with at most 2 distinct elements is [1,2,1,2] (length 4).

**Output:**
```typescript
4
```

---

### **Example 2**

**Input:**
```typescript
nums = [1, 2, 1, 3, 4]
k = 2
```
**Explanation:**
- The longest subarray with at most 2 distinct elements is [1,2,1] (length 3).

**Output:**
```typescript
3
```

---

### **Constraints**
* `1 <= nums.length <= 10^5`
* `1 <= k <= nums.length`
* `1 <= nums[i] <= 10^5`

---

### **Function Signature (TypeScript)**
```typescript
function longestSubarrayWithKDistinct(nums: number[], k: number): number
```

---

### **Starter Code**
```typescript
function longestSubarrayWithKDistinct(nums: number[], k: number): number {
    // Write your code here
    return 0;
}

// Example
console.log(longestSubarrayWithKDistinct([1, 2, 1, 2, 3], 2)); // Expected output: 4
console.log(longestSubarrayWithKDistinct([1, 2, 1, 3, 4], 2)); // Expected output: 3
```

---

### 💡 **Hints**
* Use a sliding window and a hash map to track the count of each element in the window.
* When the window has more than k distinct elements, shrink it from the left.
* This can be solved in O(n) time.
