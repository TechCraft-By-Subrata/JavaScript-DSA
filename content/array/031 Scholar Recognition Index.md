**Difficulty:** Intermediate
## 🧩 Problem: "Scholar Recognition Index"

### **Story**

At the Indian Science Congress, researchers are recognized based on the impact of their published papers. Each researcher wants to know their Scholar Recognition Index, which is the largest number h such that they have at least h papers with at least h citations each. Can you help the researchers calculate their index?

Your task is to compute the Scholar Recognition Index (H-Index) for the given array of citation counts.

---

### **Example 1**

**Input:**
```typescript
citations = [3,0,6,1,5]
```
**Output:**
```typescript
3
```
**Explanation:**
The researcher has 3 papers with at least 3 citations each.

---

### **Example 2**

**Input:**
```typescript
citations = [1,3,1]
```
**Output:**
```typescript
1
```
**Explanation:**
The researcher has 1 paper with at least 1 citation.

---

### **Constraints**
* `1 <= citations.length <= 5000`
* `0 <= citations[i] <= 1000`

---

### **Function Signature (TypeScript)**
```typescript
function scholarRecognitionIndex(citations: number[]): number
```

---

### **Starter Code**
```typescript
function scholarRecognitionIndex(citations: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(scholarRecognitionIndex([3,0,6,1,5])); // Expected output: 3
console.log(scholarRecognitionIndex([1,3,1])); // Expected output: 1
```

---

### 💡 **Hints**
* Sort the citations array and count from the highest.
* The index is the maximum h where citations[h-1] >= h.
* Try to solve in O(n log n) time.

---

### 🚀 Where is this asked?
This problem (H-Index) is frequently asked in coding interviews at top companies:
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

This problem is used to test sorting, counting, edge case handling, and efficient coding skills for real-world scenarios.
