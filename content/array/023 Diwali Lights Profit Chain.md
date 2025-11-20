**Difficulty:** Advanced
## 🧩 Problem: "Diwali Lights Profit Chain"

### **Story**

During Diwali in Ahmedabad, Riya is selling decorative lights. Each day, her profit or loss is recorded as an array. She wants to find the best chain of consecutive days where the product of her profits and losses is maximized. Help Riya find the maximum product of any contiguous subarray.

---

### **Example 1**

**Input:**
```typescript
profits = [2,3,-2,4]
```
**Output:**
```typescript
6
```
**Explanation:**
The best chain is [2,3], which multiplies to 6.

---

### **Example 2**

**Input:**
```typescript
profits = [-2,0,-1]
```
**Output:**
```typescript
0
```
**Explanation:**
The best chain is [0].

---

### **Constraints**
* `1 <= profits.length <= 2 * 10^4`
* `-10 <= profits[i] <= 10`

---

### **Function Signature (TypeScript)**
```typescript
function diwaliLightsProfitChain(profits: number[]): number
```

---

### **Starter Code**
```typescript
function diwaliLightsProfitChain(profits: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(diwaliLightsProfitChain([2,3,-2,4])); // Expected output: 6
console.log(diwaliLightsProfitChain([-2,0,-1])); // Expected output: 0
```

---

### 💡 **Hints**
* Track both the maximum and minimum product at each step.
* Negative numbers can flip the product, so swap when needed.
* Use dynamic programming for O(n) time.

---

### 🚀 Where is this asked?
This problem (Maximum Product Subarray) is frequently asked in coding interviews at top companies:
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
