## 🧩 Problem: "Secret Code Quartet"

### **Story**

Four puzzle masters—Ava, Ben, Chen, and Diego—are trying to unlock a vault. The vault requires a secret code: the sum of four different numbers from a list of clues must equal a target value. The masters want to know:

> Can they find **all unique groups of four clues** whose sum equals the target code?

Your task is to help the team by finding **all unique quadruplets** of clues that sum to the target. Each quadruplet should be listed in ascending order, and the overall list should not contain duplicate quadruplets.

---

### **Example 1**

**Input:**
```typescript
clues = [1, 0, -1, 0, -2, 2]
target = 0
```
**Explanation:**
- The quadruplets that sum to 0 are:
  - [-2, -1, 1, 2]
  - [-2, 0, 0, 2]
  - [-1, 0, 0, 1]

**Output:**
```typescript
[[-2, -1, 1, 2], [-2, 0, 0, 2], [-1, 0, 0, 1]]
```

---

### **Example 2**

**Input:**
```typescript
clues = [2, 2, 2, 2, 2]
target = 8
```
**Explanation:**
- Only one quadruplet: [2, 2, 2, 2]

**Output:**
```typescript
[[2, 2, 2, 2]]
```

---

### **Constraints**
* `4 <= clues.length <= 200`
* `-10^9 <= clues[i] <= 10^9`
* `-10^9 <= target <= 10^9`

---

### **Function Signature (TypeScript)**
```typescript
function secretCodeQuartet(clues: number[], target: number): number[][]
```

---

### **Starter Code**
```typescript
function secretCodeQuartet(clues: number[], target: number): number[][] {
    // Write your code here
    return [];
}

// Example
console.log(secretCodeQuartet([1, 0, -1, 0, -2, 2], 0)); // Expected output: [[-2, -1, 1, 2], [-2, 0, 0, 2], [-1, 0, 0, 1]]
console.log(secretCodeQuartet([2, 2, 2, 2, 2], 8)); // Expected output: [[2, 2, 2, 2]]
```

---

### 💡 **Hints**
* Sort the clues first to make it easier to avoid duplicates.
* Use two nested loops to fix the first two numbers, then use two pointers for the remaining two.
* Skip duplicate values to ensure unique quadruplets.
