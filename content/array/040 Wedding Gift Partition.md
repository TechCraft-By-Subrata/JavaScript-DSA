**Difficulty:** Medium
## 🧩 Problem: "Wedding Gift Partition"

### **Story**

At a Bengali wedding, the gifts are distributed among guests in pairs. Each gift has a value, and the organizers want to maximize the sum of the minimum values in each pair. Can you help them partition the gifts so that the sum of the minimums in each pair is maximized?

Given an array of gift values (even length), pair up the gifts and return the maximum possible sum of the minimums in each pair.

---

### **Example 1**

**Input:**
```typescript
gifts = [1,4,3,2]
```
**Output:**
```typescript
4
```
**Explanation:**
Pairs: (1,2), (3,4). Min values: 1, 3. Sum: 4.

---

### **Example 2**

**Input:**
```typescript
gifts = [6,2,6,5,1,2]
```
**Output:**
```typescript
9
```
**Explanation:**
Pairs: (1,2), (2,5), (6,6). Min values: 1,2,6. Sum: 9.

---

### **Constraints**
* `1 <= gifts.length <= 10^4`
* `gifts.length` is even
* `-10^4 <= gifts[i] <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function weddingGiftPartition(gifts: number[]): number
```

---

### **Starter Code**
```typescript
function weddingGiftPartition(gifts: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(weddingGiftPartition([1,4,3,2])); // Expected output: 4
console.log(weddingGiftPartition([6,2,6,5,1,2])); // Expected output: 9
```

---

### 💡 **Hints**
* Sort the array and pair consecutive elements.
* Try to solve in O(n log n) time.

---

### 🚀 Where is this asked?
This problem (Array Partition I) is frequently asked in coding interviews at top companies:
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

This problem is used to test sorting, greedy pairing, and edge case handling for real-world scenarios.
