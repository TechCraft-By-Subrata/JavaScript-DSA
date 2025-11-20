**Difficulty:** Advanced
## 🧩 Problem: "Monsoon Puddle Collector"

### **Story**

During the monsoon season in Kochi, Aarush and his friends are playing outside. They notice that after a heavy rain, water gets trapped between the uneven heights of the pavement stones, forming puddles. Aarush wonders: if he knows the heights of the stones, can he calculate how much rainwater will be trapped after the downpour?

Your task is to help Aarush by finding the total amount of rainwater that can be trapped between the stones, given their heights as an array.

---

### **Example 1**

**Input:**
```typescript
heights = [0,1,0,2,1,0,1,3,2,1,2,1]
```
**Output:**
```typescript
6
```

---

### **Example 2**

**Input:**
```typescript
heights = [4,2,0,3,2,5]
```
**Output:**
```typescript
9
```

---

### **Constraints**
* `1 <= heights.length <= 2 * 10^4`
* `0 <= heights[i] <= 10^5`

---

### **Function Signature (TypeScript)**
```typescript
function monsoonPuddleCollector(heights: number[]): number
```

---

### **Starter Code**
```typescript
function monsoonPuddleCollector(heights: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(monsoonPuddleCollector([0,1,0,2,1,0,1,3,2,1,2,1])); // Expected output: 6
console.log(monsoonPuddleCollector([4,2,0,3,2,5])); // Expected output: 9
```

---

### 💡 **Hints**
* Use two pointers to scan from both ends and keep track of the maximum heights.
* Water trapped at each position depends on the minimum of the max heights to the left and right.
* Try to solve in O(n) time and O(1) space.

---

### 🚀 Where is this asked?
This problem (Trapping Rain Water) is frequently asked in coding interviews at top companies:
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

This problem is used to test advanced two-pointer techniques, edge case handling, and efficient coding skills for real-world scenarios.
