**Difficulty:** Advanced
## 🧩 Problem: "Festival Group Harmony"

### **Story**

At the Goa Carnival, groups of performers want to form the largest harmonious group possible. Each performer has a unique number, and a group is harmonious if for every pair of performers in the group, one number divides the other. Can you help the organizers find the largest harmonious group?

Your task is to return the largest subset of numbers such that for every pair (Si, Sj) in the subset, either Si % Sj == 0 or Sj % Si == 0.

---

### **Example 1**

**Input:**
```typescript
performers = [1,2,3]
```
**Output:**
```typescript
[1,2]
```
**Explanation:**
The largest harmonious group is [1,2].

---

### **Example 2**

**Input:**
```typescript
performers = [1,2,4,8]
```
**Output:**
```typescript
[1,2,4,8]
```
**Explanation:**
All numbers divide each other in sequence.

---

### **Constraints**
* `1 <= performers.length <= 1000`
* `1 <= performers[i] <= 2 * 10^9`

---

### **Function Signature (TypeScript)**
```typescript
function festivalGroupHarmony(performers: number[]): number[]
```

---

### **Starter Code**
```typescript
function festivalGroupHarmony(performers: number[]): number[] {
    // Write your code here
    return [];
}

// Example
console.log(festivalGroupHarmony([1,2,3])); // Expected output: [1,2]
console.log(festivalGroupHarmony([1,2,4,8])); // Expected output: [1,2,4,8]
```

---

### 💡 **Hints**
* Sort the array and use dynamic programming to build up the largest subset.
* For each number, check if it can be added to the subset ending with a smaller number.
* Try to solve in O(n^2) time.

---

### 🚀 Where is this asked?
This problem (Largest Divisible Subset) is frequently asked in coding interviews at top companies:
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

This problem is used to test dynamic programming, divisibility logic, edge case handling, and efficient coding skills for real-world scenarios.
