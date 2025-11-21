**Difficulty:** Advanced
## 🧩 Problem: "Parade Float Popularity"

### **Story**

During the Ganesh Chaturthi parade in Pune, each float is rated by the crowd. Organizers want to know, for each float, how many floats with lower ratings come after it in the parade. Can you help them calculate the popularity count for each float?

Your task is to return an array where each element is the number of floats with a lower rating that appear after it in the array.

---

### **Example 1**

**Input:**
```typescript
ratings = [5,2,6,1]
```
**Output:**
```typescript
[2,1,1,0]
```
**Explanation:**
- For 5: floats 2 and 1 are smaller and come after
- For 2: float 1 is smaller and comes after
- For 6: float 1 is smaller and comes after
- For 1: none are smaller after

---

### **Example 2**

**Input:**
```typescript
ratings = [-1,-1]
```
**Output:**
```typescript
[0,0]
```

---

### **Constraints**
* `1 <= ratings.length <= 10^5`
* `-10^4 <= ratings[i] <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function paradeFloatPopularity(ratings: number[]): number[]
```

---

### **Starter Code**
```typescript
function paradeFloatPopularity(ratings: number[]): number[] {
    // Write your code here
    return [];
}

// Example
console.log(paradeFloatPopularity([5,2,6,1])); // Expected output: [2,1,1,0]
console.log(paradeFloatPopularity([-1,-1])); // Expected output: [0,0]
```

---

### 💡 **Hints**
* Use a Binary Indexed Tree (Fenwick Tree) or a modified merge sort for O(n log n) solution.
* Count and update the number of smaller elements as you process from right to left.
* Try to solve in O(n log n) time.

---

### 🚀 Where is this asked?
This problem (Count of Smaller Numbers After Self) is frequently asked in coding interviews at top companies:
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

This problem is used to test advanced data structures, merge sort, edge case handling, and efficient coding skills for real-world scenarios.
