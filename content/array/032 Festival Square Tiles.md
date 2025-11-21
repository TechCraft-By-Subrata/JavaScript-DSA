**Difficulty:** Intermediate
## 🧩 Problem: "Festival Square Tiles"

### **Story**

At the Pushkar Camel Fair, organizers are laying out square tiles to cover the ground for a dance performance. Given a number n, they want to use the minimum number of perfect square tiles (like 1x1, 2x2, 3x3, etc.) to cover exactly n square units. Can you help them find the minimum number of tiles needed?

Your task is to find the least number of perfect square numbers that sum to n.

---

### **Example 1**

**Input:**
```typescript
n = 12
```
**Output:**
```typescript
3
```
**Explanation:**
12 = 4 + 4 + 4

---

### **Example 2**

**Input:**
```typescript
n = 13
```
**Output:**
```typescript
2
```
**Explanation:**
13 = 4 + 9

---

### **Constraints**
* `1 <= n <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function festivalSquareTiles(n: number): number
```

---

### **Starter Code**
```typescript
function festivalSquareTiles(n: number): number {
    // Write your code here
    return 0;
}

// Example
console.log(festivalSquareTiles(12)); // Expected output: 3
console.log(festivalSquareTiles(13)); // Expected output: 2
```

---

### 💡 **Hints**
* Use dynamic programming to build up the solution.
* For each number, try subtracting all possible square numbers.
* Try to solve in O(n√n) time.

---

### 🚀 Where is this asked?
This problem (Perfect Squares) is frequently asked in coding interviews at top companies:
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

This problem is used to test dynamic programming, edge case handling, and efficient coding skills for real-world scenarios.
