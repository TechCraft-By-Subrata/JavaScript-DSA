**Difficulty:** Intermediate
## 🧩 Problem: "Grand Wedding Spiral Walk"

### **Story**

At a grand wedding in Udaipur, the banquet hall is decorated with a large rectangular arrangement of tables, each with a unique number. Aarav and his cousins are challenged to collect sweets from the tables by walking in a spiral pattern, starting from the top-left and moving inward. Can you help Aarav list the table numbers in the exact order they should walk to collect all the sweets in a spiral?

Your task is to return the spiral order of the numbers in the given matrix.

---

### **Example 1**

**Input:**
```typescript
matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
]
```
**Output:**
```typescript
[1,2,3,6,9,8,7,4,5]
```

---

### **Example 2**

**Input:**
```typescript
matrix = [
  [1, 2, 3, 4],
  [5, 6, 7, 8],
  [9,10,11,12]
]
```
**Output:**
```typescript
[1,2,3,4,8,12,11,10,9,5,6,7]
```

---

### **Constraints**
* `1 <= matrix.length, matrix[0].length <= 100`
* `-10^4 <= matrix[i][j] <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function grandWeddingSpiralWalk(matrix: number[][]): number[]
```

---

### **Starter Code**
```typescript
function grandWeddingSpiralWalk(matrix: number[][]): number[] {
    // Write your code here
    return [];
}

// Example
console.log(grandWeddingSpiralWalk([
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
])); // Expected output: [1,2,3,6,9,8,7,4,5]
console.log(grandWeddingSpiralWalk([
  [1, 2, 3, 4],
  [5, 6, 7, 8],
  [9,10,11,12]
])); // Expected output: [1,2,3,4,8,12,11,10,9,5,6,7]
```

---

### 💡 **Hints**
* Use four pointers to keep track of the current boundaries.
* Traverse the matrix layer by layer, moving right, down, left, and up.
* Stop when all elements are visited.

---

### 🚀 Where is this asked?
This problem (Spiral Matrix) is frequently asked in coding interviews at top companies:
- Google
- Amazon
- Microsoft
- Facebook
- Flipkart
- Goldman Sachs
- Uber
- Atlassian
- Paytm
- Swiggy
- Zomato
- Apple
- Adobe
- Oracle
- Infosys
- TCS
- Cognizant
- Capgemini
- HCL Technologies
- Wipro
- JP Morgan Chase
- Morgan Stanley
- HSBC
- SAP
- Salesforce
- LinkedIn
- Twitter
- Meesho
- Razorpay
- PhonePe
- Byju's
- Dream11
- InMobi
- Ola
- Oyo
- Practo
- Freshworks
- Mindtree
- L&T Infotech

**Relevant Roles:**
- Software Engineer (SDE)
- Backend Developer
- Frontend Developer
- Data Scientist
- Algorithm Engineer
- Full Stack Developer
- Machine Learning Engineer
- Product Engineer
- Technical Lead
- Solution Architect

This problem is used to test matrix traversal, edge case handling, and efficient coding skills for real-world scenarios.
