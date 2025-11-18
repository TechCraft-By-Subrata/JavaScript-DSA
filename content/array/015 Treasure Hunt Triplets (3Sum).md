## 🧩 Problem: "Treasure Hunt Triplets"

### **Story**

Three friends—Sam, Priya, and Leo—are on a treasure hunt. They have a map with a list of clues, each clue is a number. The goal is to find all unique groups of three clues that, when combined, lead to a total value of zero (the secret code to unlock the treasure chest).

Your task is to help the friends by finding **all unique triplets** of clues whose sum is zero. Each triplet should be listed in ascending order, and the overall list should not contain duplicate triplets.

---

### **Example 1**

**Input:**
```typescript
clues = [-1, 0, 1, 2, -1, -4]
```
**Explanation:**
- The triplets that sum to zero are:
  - [-1, 0, 1]
  - [-1, -1, 2]

**Output:**
```typescript
[[-1, -1, 2], [-1, 0, 1]]
```

---

### **Example 2**

**Input:**
```typescript
clues = [0, 1, 1]
```
**Explanation:**
- No triplet sums to zero.

**Output:**
```typescript
[]
```

---

### **Example 3**

**Input:**
```typescript
clues = [0, 0, 0]
```
**Explanation:**
- Only one triplet: [0, 0, 0]

**Output:**
```typescript
[[0, 0, 0]]
```

---

### **Constraints**
* `3 <= clues.length <= 3000`
* `-10^5 <= clues[i] <= 10^5`

---

### **Function Signature (TypeScript)**
```typescript
function treasureHuntTriplets(clues: number[]): number[][]
```

---

### **Starter Code**
```typescript
function treasureHuntTriplets(clues: number[]): number[][] {
    // Write your code here
    return [];
}

// Example
console.log(treasureHuntTriplets([-1, 0, 1, 2, -1, -4])); // Expected output: [[-1, -1, 2], [-1, 0, 1]]
console.log(treasureHuntTriplets([0, 1, 1])); // Expected output: []
console.log(treasureHuntTriplets([0, 0, 0])); // Expected output: [[0, 0, 0]]
```

---

### 💡 **Hints**
* Sort the clues first to make it easier to avoid duplicates.
* Use two pointers for each fixed clue to find pairs that sum to the negative of the fixed clue.
* Skip duplicate values to ensure unique triplets.
