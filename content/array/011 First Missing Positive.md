**Difficulty:** Advanced
## 🧩 Problem: "The Missing Registration ID"

### **Story**

In the vibrant city of Pune, Meera is organizing a coding contest for school students. Each participant is assigned a unique positive number as their registration ID. However, due to a technical glitch, some IDs are missing from the list. Meera wants to quickly find the smallest missing positive registration ID so she can assign it to the next participant.

Your task is to help Meera by finding the smallest missing positive integer from the list of registration IDs.

---

### **Example 1**

**Input:**
```typescript
ids = [1,2,0]
```
**Output:**
```typescript
3
```

---

### **Example 2**

**Input:**
```typescript
ids = [3,4,-1,1]
```
**Output:**
```typescript
2
```

---

### **Example 3**

**Input:**
```typescript
ids = [7,8,9,11,12]
```
**Output:**
```typescript
1
```

---

### **Constraints**
* `1 <= ids.length <= 10^5`
* `-10^6 <= ids[i] <= 10^6`

---

### **Function Signature (TypeScript)**
```typescript
function missingRegistrationID(ids: number[]): number
```

---

### **Starter Code**
```typescript
function missingRegistrationID(ids: number[]): number {
    // Write your code here
    return 1;
}

// Example
console.log(missingRegistrationID([1,2,0])); // Expected output: 3
console.log(missingRegistrationID([3,4,-1,1])); // Expected output: 2
console.log(missingRegistrationID([7,8,9,11,12])); // Expected output: 1
```

---

### 💡 **Hints**
* Try to solve the problem in O(n) time and constant space.
* Place each number in its correct index if possible.
* Ignore negative numbers and numbers greater than the array length.

---

### 🚀 Where is this asked?
This problem (First Missing Positive) is frequently asked in coding interviews at top companies:
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

This problem is used to test advanced array manipulation, edge case handling, and efficient coding skills for real-world scenarios.
