**Difficulty:** Intermediate
## 🧩 Problem: "Prize Winner Selection"

### **Story**

At a school fest in Chandigarh, the organizers have a list of scores from various competitions. To select the prize winners, they want to find the Kth largest score in the list. Can you help the organizers quickly determine the Kth largest score?

Your task is to find the Kth largest element in the array of scores.

---

### **Example 1**

**Input:**
```typescript
scores = [3,2,1,5,6,4]
k = 2
```
**Output:**
```typescript
5
```
**Explanation:**
The 2nd largest score is 5.

---

### **Example 2**

**Input:**
```typescript
scores = [3,2,3,1,2,4,5,5,6]
k = 4
```
**Output:**
```typescript
4
```
**Explanation:**
The 4th largest score is 4.

---

### **Constraints**
* `1 <= k <= scores.length <= 10^5`
* `-10^4 <= scores[i] <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function prizeWinnerSelection(scores: number[], k: number): number
```

---

### **Starter Code**
```typescript
function prizeWinnerSelection(scores: number[], k: number): number {
    // Write your code here
    return 0;
}

// Example
console.log(prizeWinnerSelection([3,2,1,5,6,4], 2)); // Expected output: 5
console.log(prizeWinnerSelection([3,2,3,1,2,4,5,5,6], 4)); // Expected output: 4
```

---

### 💡 **Hints**
* Use a min-heap of size k for efficient solution.
* Quickselect algorithm can also be used for average O(n) time.
* Sorting the array is a simple but less efficient approach.

---

### 🚀 Where is this asked?
This problem (Kth Largest Element in an Array) is frequently asked in coding interviews at top companies:
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

This problem is used to test heap, quickselect, sorting, edge case handling, and efficient coding skills for real-world scenarios.
