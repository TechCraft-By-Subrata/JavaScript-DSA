**Difficulty:** Intermediate
## 🧩 Problem: "Royal Banquet Spiral Fill"

### **Story**

At the royal palace in Mysuru, the banquet hall is being prepared for a grand feast. The tables are arranged in an empty square grid, and the staff must place numbered plates in a spiral order, starting from 1 and filling up to n². Can you help the staff fill the grid in spiral order?

Your task is to generate an n x n matrix filled with numbers from 1 to n² in spiral order.

---

### **Example 1**

**Input:**
```typescript
n = 3
```
**Output:**
```typescript
[
  [1,2,3],
  [8,9,4],
  [7,6,5]
]
```

---

### **Example 2**

**Input:**
```typescript
n = 1
```
**Output:**
```typescript
[[1]]
```

---

### **Constraints**
* `1 <= n <= 100`

---

### **Function Signature (TypeScript)**
```typescript
function royalBanquetSpiralFill(n: number): number[][]
```

---

### **Starter Code**
```typescript
function royalBanquetSpiralFill(n: number): number[][] {
    // Write your code here
    return [];
}

// Example
console.log(royalBanquetSpiralFill(3)); // Expected output: [[1,2,3],[8,9,4],[7,6,5]]
console.log(royalBanquetSpiralFill(1)); // Expected output: [[1]]
```

---

### 💡 **Hints**
* Use four pointers to keep track of the current boundaries.
* Fill the matrix layer by layer, moving right, down, left, and up.
* Stop when all numbers are placed.

---

### 🚀 Where is this asked?
This problem (Spiral Matrix II) is frequently asked in coding interviews at top companies:
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

This problem is used to test matrix construction, edge case handling, and efficient coding skills for real-world scenarios.
