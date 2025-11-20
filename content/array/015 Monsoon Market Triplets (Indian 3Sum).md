**Difficulty:** Intermediate
## 🧩 Problem: "Monsoon Market Triplets"

### **Story**

Three friends—Amit, Kavya, and Farhan—are exploring the bustling monsoon market in Mumbai. Each stall offers a clue in the form of a number. The trio believes that if they can find three clues whose sum is exactly zero, they will unlock a special festival prize from the market organizer.

Your task is to help Amit, Kavya, and Farhan by finding **all unique triplets** of clues whose sum is zero. Each triplet should be listed in ascending order, and the overall list should not contain duplicate triplets.

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
function monsoonMarketTriplets(clues: number[]): number[][]
```

---

### **Starter Code**
```typescript
function monsoonMarketTriplets(clues: number[]): number[][] {
    // Write your code here
    return [];
}

// Example
console.log(monsoonMarketTriplets([-1, 0, 1, 2, -1, -4])); // Expected output: [[-1, -1, 2], [-1, 0, 1]]
console.log(monsoonMarketTriplets([0, 1, 1])); // Expected output: []
console.log(monsoonMarketTriplets([0, 0, 0])); // Expected output: [[0, 0, 0]]
```

---

### 💡 **Hints**
* Sort the clues first to make it easier to avoid duplicates.
* Use two pointers for each fixed clue to find pairs that sum to the negative of the fixed clue.
* Skip duplicate values to ensure unique triplets.

---

### 🚀 Where is this asked?
This problem (3Sum) is a favorite in coding interviews at top companies:
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

This problem is used to test deeper problem-solving skills, handling edge cases, and writing efficient code for real-world scenarios.
