**Difficulty:** Advanced
## 🧩 Problem: "Bazaar Product Challenge"

### **Story**

At the bustling Dilli Haat bazaar, vendors are comparing their daily sales. Each vendor's sales are recorded in an array. For a special contest, each vendor wants to know the product of all other vendors' sales except their own, for every position in the array. Can you help the vendors calculate this efficiently?

Your task is to return an array where each element is the product of all other elements except itself.

---

### **Example 1**

**Input:**
```typescript
sales = [1,2,3,4]
```
**Output:**
```typescript
[24,12,8,6]
```
**Explanation:**
- For index 0: 2*3*4 = 24
- For index 1: 1*3*4 = 12
- For index 2: 1*2*4 = 8
- For index 3: 1*2*3 = 6

---

### **Example 2**

**Input:**
```typescript
sales = [-1,1,0,-3,3]
```
**Output:**
```typescript
[0,0,9,0,0]
```

---

### **Constraints**
* `2 <= sales.length <= 10^5`
* `-30 <= sales[i] <= 30`
* The product of any prefix or suffix of sales will fit in a 32-bit integer.

---

### **Function Signature (TypeScript)**
```typescript
function bazaarProductChallenge(sales: number[]): number[]
```

---

### **Starter Code**
```typescript
function bazaarProductChallenge(sales: number[]): number[] {
    // Write your code here
    return [];
}

// Example
console.log(bazaarProductChallenge([1,2,3,4])); // Expected output: [24,12,8,6]
console.log(bazaarProductChallenge([-1,1,0,-3,3])); // Expected output: [0,0,9,0,0]
```

---

### 💡 **Hints**
* Use prefix and suffix products to avoid division.
* Build the result in two passes: left-to-right and right-to-left.
* Try to solve in O(n) time and O(1) extra space (excluding output array).

---

### 🚀 Where is this asked?
This problem (Product of Array Except Self) is frequently asked in coding interviews at top companies:
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

This problem is used to test prefix/suffix product techniques, edge case handling, and efficient coding skills for real-world scenarios.
