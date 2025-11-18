## 🧩 Problem: "Subarray Sum Equals K"

### **Problem Description**

You are given an array of integers `nums` and an integer `k`.
Your task is to find the **number of contiguous subarrays** whose sum equals `k`.

Return the **count** of such subarrays.

---

### **Example 1**

**Input:**
```typescript
nums = [1, 2, 3]
k = 3
```
**Explanation:**
- Subarrays: [1,2], [3]
- [1,2] sum = 3
- [3] sum = 3
- Total: 2 subarrays

**Output:**
```typescript
2
```

---

### **Example 2**

**Input:**
```typescript
nums = [1, 1, 1]
k = 2
```
**Explanation:**
- Subarrays: [1,1] (at index 0-1), [1,1] (at index 1-2)
- Total: 2 subarrays

**Output:**
```typescript
2
```

---

### **Constraints**
* `1 <= nums.length <= 10^4`
* `-10^4 <= nums[i], k <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function subarraySum(nums: number[], k: number): number
```

---

### **Starter Code**
```typescript
function subarraySum(nums: number[], k: number): number {
    // Write your code here
    return 0;
}

// Example
console.log(subarraySum([1, 2, 3], 3)); // Expected output: 2
console.log(subarraySum([1, 1, 1], 2)); // Expected output: 2
```

---

### 💡 **Hints**
* Use a running sum and a hash map to store the frequency of prefix sums.
* For each index, check if (current_sum - k) exists in the map.
* This can be solved in O(n) time.
