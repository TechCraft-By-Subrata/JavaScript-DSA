**Difficulty:** Easy
## 🧩 Problem: "Holi Shuffle Parade"

### **Story**

During Holi in Mathura, children shuffle colored parade floats in a special way. Given an array of 2n elements in the form [x1,x2,...,xn,y1,y2,...,yn], they want to rearrange it to [x1,y1,x2,y2,...,xn,yn]. Can you help them shuffle the parade floats?

Given an array of 2n elements, return the shuffled array as described.

---

### **Example 1**

**Input:**
```typescript
floats = [2,5,1,3,4,7], n = 3
```
**Output:**
```typescript
[2,3,5,4,1,7]
```
**Explanation:**
Floats are shuffled as per the Holi parade.

---

### **Constraints**
* `1 <= n <= 500`
* `floats.length == 2n`
* `1 <= floats[i] <= 10^3`

---

### **Function Signature (TypeScript)**
```typescript
function holiShuffleParade(floats: number[], n: number): number[]
```

---

### **Starter Code**
```typescript
function holiShuffleParade(floats: number[], n: number): number[] {
    // Write your code here
    return [];
}

// Example
console.log(holiShuffleParade([2,5,1,3,4,7], 3)); // Expected output: [2,3,5,4,1,7]
```

---

### 💡 **Hints**
* Use a simple loop to interleave elements.
* No extra space needed except for the result array.

---

### 🚀 Where is this asked?
This problem (Shuffle the Array) is frequently asked in coding interviews at top companies:
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

This problem is used to test array manipulation, indexing, and efficient coding skills for real-world scenarios.
