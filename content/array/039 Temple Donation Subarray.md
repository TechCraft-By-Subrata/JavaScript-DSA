**Difficulty:** Advanced
## 🧩 Problem: "Temple Donation Subarray"

### **Story**

During the annual festival at the Tirupati temple, devotees make donations in a sequence. The temple committee wants to find the number of continuous donation streaks that sum up to exactly ₹K. Can you help them count the number of such subarrays?

Given an array of donations and an integer K, return the total number of continuous subarrays whose sum equals K.

---

### **Example 1**

**Input:**
```typescript
donations = [1,2,3], K = 3
```
**Output:**
```typescript
2
```
**Explanation:**
The subarrays [1,2] and [3] both sum to 3.

---

### **Example 2**

**Input:**
```typescript
donations = [1,1,1], K = 2
```
**Output:**
```typescript
2
```
**Explanation:**
The subarrays [1,1] (twice) sum to 2.

---

### **Constraints**
* `1 <= donations.length <= 10^5`
* `-10^4 <= donations[i] <= 10^4`
* `-10^7 <= K <= 10^7`

---

### **Function Signature (TypeScript)**
```typescript
function templeDonationSubarray(donations: number[], K: number): number
```

---

### **Starter Code**
```typescript
function templeDonationSubarray(donations: number[], K: number): number {
    // Write your code here
    return 0;
}

// Example
console.log(templeDonationSubarray([1,2,3], 3)); // Expected output: 2
console.log(templeDonationSubarray([1,1,1], 2)); // Expected output: 2
```

---

### 💡 **Hints**
* Use a hash map to store prefix sums.
* Try to solve in O(n) time.
* Consider edge cases with negative numbers.

---

### 🚀 Where is this asked?
This problem (Subarray Sum Equals K) is frequently asked in coding interviews at top companies:
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
