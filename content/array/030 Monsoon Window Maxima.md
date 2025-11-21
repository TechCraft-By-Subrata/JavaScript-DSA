**Difficulty:** Advanced
## 🧩 Problem: "Monsoon Window Maxima"

### **Story**

During the monsoon in Mumbai, weather stations record daily rainfall amounts. To analyze the heaviest spells, meteorologist Kavya wants to know the maximum rainfall in every window of k consecutive days. Can you help Kavya efficiently find the maximum for each window?

Your task is to return an array of the maximum rainfall for each sliding window of size k.

---

### **Example 1**

**Input:**
```typescript
rainfall = [1,3,-1,-3,5,3,6,7]
k = 3
```
**Output:**
```typescript
[3,3,5,5,6,7]
```
**Explanation:**
- Window [1,3,-1] → max is 3
- Window [3,-1,-3] → max is 3
- Window [-1,-3,5] → max is 5
- Window [-3,5,3] → max is 5
- Window [5,3,6] → max is 6
- Window [3,6,7] → max is 7

---

### **Example 2**

**Input:**
```typescript
rainfall = [1]
k = 1
```
**Output:**
```typescript
[1]
```

---

### **Constraints**
* `1 <= rainfall.length <= 10^5`
* `-10^4 <= rainfall[i] <= 10^4`
* `1 <= k <= rainfall.length`

---

### **Function Signature (TypeScript)**
```typescript
function monsoonWindowMaxima(rainfall: number[], k: number): number[]
```

---

### **Starter Code**
```typescript
function monsoonWindowMaxima(rainfall: number[], k: number): number[] {
    // Write your code here
    return [];
}

// Example
console.log(monsoonWindowMaxima([1,3,-1,-3,5,3,6,7], 3)); // Expected output: [3,3,5,5,6,7]
console.log(monsoonWindowMaxima([1], 1)); // Expected output: [1]
```

---

### 💡 **Hints**
* Use a deque to keep track of indices of useful elements.
* Remove indices that are out of the current window.
* Try to solve in O(n) time.

---

### 🚀 Where is this asked?
This problem (Sliding Window Maximum) is frequently asked in coding interviews at top companies:
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

This problem is used to test deque usage, sliding window techniques, edge case handling, and efficient coding skills for real-world scenarios.
