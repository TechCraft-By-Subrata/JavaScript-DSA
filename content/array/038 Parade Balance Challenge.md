**Difficulty:** Advanced
## 🧩 Problem: "Parade Balance Challenge"

### **Story**

During the Independence Day parade in Chennai, the organizers want to balance the number of floats with the Indian flag and those with the state flag. Each float is marked as 0 (state flag) or 1 (Indian flag). Can you help them find the length of the longest contiguous segment where the number of state and Indian flag floats is equal?

Your task is to return the length of the longest contiguous subarray with equal numbers of 0s and 1s.

---

### **Example 1**

**Input:**
```typescript
floats = [0,1]
```
**Output:**
```typescript
2
```
**Explanation:**
Both floats are balanced.

---

### **Example 2**

**Input:**
```typescript
floats = [0,1,0]
```
**Output:**
```typescript
2
```
**Explanation:**
The longest balanced segment is [0,1] or [1,0].

---

### **Constraints**
* `1 <= floats.length <= 10^5`
* `floats[i]` is 0 or 1

---

### **Function Signature (TypeScript)**
```typescript
function paradeBalanceChallenge(floats: number[]): number
```

---

### **Starter Code**
```typescript
function paradeBalanceChallenge(floats: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(paradeBalanceChallenge([0,1])); // Expected output: 2
console.log(paradeBalanceChallenge([0,1,0])); // Expected output: 2
```

---

### 💡 **Hints**
* Use a hash map to track the first occurrence of each count difference.
* Convert 0s to -1s to simplify the problem.
* Try to solve in O(n) time.

---

### 🚀 Where is this asked?
This problem (Contiguous Array) is frequently asked in coding interviews at top companies:
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

This problem is used to test hash map usage, prefix sum, edge case handling, and efficient coding skills for real-world scenarios.
