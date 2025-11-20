**Difficulty:** Intermediate
## 🧩 Problem: "Festival Profit Streak"

### **Story**

During the festive season in Surat, Priyansh is running a series of food stalls. Each day, he records his profit or loss. He wants to know the best streak of consecutive days where his total profit is maximized. Help Priyansh find the maximum sum of any contiguous subarray of profits and losses.

---

### **Example 1**

**Input:**
```typescript
profits = [-2,1,-3,4,-1,2,1,-5,4]
```
**Output:**
```typescript
6
```
**Explanation:**
The best streak is [4,-1,2,1], which sums to 6.

---

### **Example 2**

**Input:**
```typescript
profits = [1]
```
**Output:**
```typescript
1
```

---

### **Constraints**
* `1 <= profits.length <= 10^5`
* `-10^4 <= profits[i] <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function festivalProfitStreak(profits: number[]): number
```

---

### **Starter Code**
```typescript
function festivalProfitStreak(profits: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(festivalProfitStreak([-2,1,-3,4,-1,2,1,-5,4])); // Expected output: 6
console.log(festivalProfitStreak([1])); // Expected output: 1
```

---

### 💡 **Hints**
* Use Kadane's algorithm for O(n) time complexity.
* Keep track of the current sum and the maximum sum so far.
* Reset the current sum if it drops below zero.

---

### 🚀 Where is this asked?
This problem (Maximum Subarray) is frequently asked in coding interviews at top companies:
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
