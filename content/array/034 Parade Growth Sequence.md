**Difficulty:** Advanced
## 🧩 Problem: "Parade Growth Sequence"

### **Story**

At the Republic Day parade in Delhi, the organizers want to arrange floats in a way that each subsequent float is taller than the previous one, forming the longest possible increasing sequence. Given the heights of the floats, can you help them find the length of the longest increasing subsequence?

Your task is to find the length of the longest strictly increasing subsequence in the array of float heights.

---

### **Example 1**

**Input:**
```typescript
floats = [10,9,2,5,3,7,101,18]
```
**Output:**
```typescript
4
```
**Explanation:**
The longest increasing subsequence is [2,3,7,101].

---

### **Example 2**

**Input:**
```typescript
floats = [0,1,0,3,2,3]
```
**Output:**
```typescript
4
```
**Explanation:**
The longest increasing subsequence is [0,1,2,3].

---

### **Constraints**
* `1 <= floats.length <= 2500`
* `-10^4 <= floats[i] <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function paradeGrowthSequence(floats: number[]): number
```

---

### **Starter Code**
```typescript
function paradeGrowthSequence(floats: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(paradeGrowthSequence([10,9,2,5,3,7,101,18])); // Expected output: 4
console.log(paradeGrowthSequence([0,1,0,3,2,3])); // Expected output: 4
```

---

### 💡 **Hints**
* Use dynamic programming or patience sorting for O(n log n) solution.
* For each float, keep track of the smallest possible tail of all increasing subsequences of different lengths.
* Try to solve in O(n log n) time.

---

### 🚀 Where is this asked?
This problem (Longest Increasing Subsequence) is frequently asked in coding interviews at top companies:
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

This problem is used to test dynamic programming, patience sorting, edge case handling, and efficient coding skills for real-world scenarios.
