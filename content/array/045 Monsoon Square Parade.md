**Difficulty:** Easy
## 🧩 Problem: "Monsoon Square Parade"

### **Story**

During the monsoon festival in Mumbai, children arrange parade floats in a line. Each float has a number, and they want to know the squares of each float's number, arranged in non-decreasing order. Can you help them?

Given a sorted array of integers, return an array of the squares of each number sorted in non-decreasing order.

---

### **Example 1**

**Input:**
```typescript
floats = [-4,-1,0,3,10]
```
**Output:**
```typescript
[0,1,9,16,100]
```
**Explanation:**
Squares of floats sorted.

---

### **Example 2**

**Input:**
```typescript
floats = [-7,-3,2,3,11]
```
**Output:**
```typescript
[4,9,9,49,121]
```
**Explanation:**
Squares of floats sorted.

---

### **Constraints**
* `1 <= floats.length <= 10^4`
* `-10^4 <= floats[i] <= 10^4`
* `floats` is sorted in non-decreasing order

---

### **Function Signature (TypeScript)**
```typescript
function monsoonSquareParade(floats: number[]): number[]
```

---

### **Starter Code**
```typescript
function monsoonSquareParade(floats: number[]): number[] {
    // Write your code here
    return [];
}

// Example
console.log(monsoonSquareParade([-4,-1,0,3,10])); // Expected output: [0,1,9,16,100]
console.log(monsoonSquareParade([-7,-3,2,3,11])); // Expected output: [4,9,9,49,121]
```

---

### 💡 **Hints**
* Use two pointers from both ends of the array.
* Fill the result array from the end.

---

### 🚀 Where is this asked?
This problem (Squares of a Sorted Array) is frequently asked in coding interviews at top companies:
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

This problem is used to test two-pointer technique, array manipulation, and efficient coding skills for real-world scenarios.
