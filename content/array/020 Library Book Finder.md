**Difficulty:** Intermediate
## 🧩 Problem: "Library Book Finder"

### **Story**

In the grand library of Kolkata, books are arranged in a 2D grid of shelves. Each row is sorted in ascending order, and the first book of each row is greater than the last book of the previous row. Priya wants to quickly find if a particular book ID exists in the library. Can you help Priya search for the book efficiently?

Your task is to determine if the target book ID exists in the 2D matrix.

---

### **Example 1**

**Input:**
```typescript
matrix = [
  [1, 3, 5, 7],
  [10, 11, 16, 20],
  [23, 30, 34, 60]
]
target = 3
```
**Output:**
```typescript
true
```

---

### **Example 2**

**Input:**
```typescript
matrix = [
  [1, 3, 5, 7],
  [10, 11, 16, 20],
  [23, 30, 34, 60]
]
target = 13
```
**Output:**
```typescript
false
```

---

### **Constraints**
* `1 <= matrix.length, matrix[0].length <= 100`
* `-10^4 <= matrix[i][j], target <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function libraryBookFinder(matrix: number[][], target: number): boolean
```

---

### **Starter Code**
```typescript
function libraryBookFinder(matrix: number[][], target: number): boolean {
    // Write your code here
    return false;
}

// Example
console.log(libraryBookFinder([
  [1, 3, 5, 7],
  [10, 11, 16, 20],
  [23, 30, 34, 60]
], 3)); // Expected output: true
console.log(libraryBookFinder([
  [1, 3, 5, 7],
  [10, 11, 16, 20],
  [23, 30, 34, 60]
], 13)); // Expected output: false
```

---

### 💡 **Hints**
* Treat the matrix as a flattened sorted array and use binary search.
* Calculate row and column indices from the 1D index.
* Try to solve in O(log(mn)) time.

---

### 🚀 Where is this asked?
This problem (Search a 2D Matrix) is frequently asked in coding interviews at top companies:
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

This problem is used to test matrix search, binary search, edge case handling, and efficient coding skills for real-world scenarios.
