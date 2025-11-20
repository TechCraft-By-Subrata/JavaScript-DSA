**Difficulty:** Intermediate
## 🧩 Problem: "Banquet Table Cleanup"

### **Story**

At a large banquet in Chennai, the tables are arranged in a grid, and each cell represents a plate. If a plate is found to be empty (represented by zero), the staff must clean the entire row and column by setting all plates in that row and column to zero. Can you help the staff update the grid efficiently?

Your task is to set entire rows and columns to zero if any cell in them is zero, modifying the matrix in-place.

---

### **Example 1**

**Input:**
```typescript
matrix = [
  [1,1,1],
  [1,0,1],
  [1,1,1]
]
```
**Output:**
```typescript
[
  [1,0,1],
  [0,0,0],
  [1,0,1]
]
```

---

### **Example 2**

**Input:**
```typescript
matrix = [
  [0,1,2,0],
  [3,4,5,2],
  [1,3,1,5]
]
```
**Output:**
```typescript
[
  [0,0,0,0],
  [0,4,5,0],
  [0,3,1,0]
]
```

---

### **Constraints**
* `1 <= matrix.length, matrix[0].length <= 200`
* `-2^{31} <= matrix[i][j] <= 2^{31} - 1`

---

### **Function Signature (TypeScript)**
```typescript
function banquetTableCleanup(matrix: number[][]): void
```

---

### **Starter Code**
```typescript
function banquetTableCleanup(matrix: number[][]): void {
    // Write your code here
}

// Example
const m1 = [
  [1,1,1],
  [1,0,1],
  [1,1,1]
];
banquetTableCleanup(m1);
console.log(m1); // Expected output: [[1,0,1],[0,0,0],[1,0,1]]

const m2 = [
  [0,1,2,0],
  [3,4,5,2],
  [1,3,1,5]
];
banquetTableCleanup(m2);
console.log(m2); // Expected output: [[0,0,0,0],[0,4,5,0],[0,3,1,0]]
```

---

### 💡 **Hints**
* Use the first row and column as markers to reduce space usage.
* Be careful with overlapping zeros in the first row/column.
* Try to solve in O(1) additional space.

---

### 🚀 Where is this asked?
This problem (Set Matrix Zeroes) is frequently asked in coding interviews at top companies:
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

This problem is used to test matrix manipulation, edge case handling, and efficient coding skills for real-world scenarios.
