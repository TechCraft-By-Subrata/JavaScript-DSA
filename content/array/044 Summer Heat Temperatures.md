**Difficulty:** Medium
## 🧩 Problem: "Summer Heat Temperatures"

### **Story**

During the peak of summer in Rajasthan, meteorologists track daily temperatures to predict when the next hotter day will arrive. Can you help them, for each day, find out how many days they have to wait until a warmer temperature?

Given a list of daily temperatures, return a list where each element is the number of days until a warmer temperature. If there is no future day for a warmer temperature, put 0 instead.

---

### **Example 1**

**Input:**
```typescript
temperatures = [73,74,75,71,69,72,76,73]
```
**Output:**
```typescript
[1,1,4,2,1,1,0,0]
```
**Explanation:**
For each day, the output shows how many days to wait for a warmer temperature.

---

### **Constraints**
* `1 <= temperatures.length <= 10^5`
* `30 <= temperatures[i] <= 100`

---

### **Function Signature (TypeScript)**
```typescript
function summerHeatTemperatures(temperatures: number[]): number[]
```

---

### **Starter Code**
```typescript
function summerHeatTemperatures(temperatures: number[]): number[] {
    // Write your code here
    return [];
}

// Example
console.log(summerHeatTemperatures([73,74,75,71,69,72,76,73])); // Expected output: [1,1,4,2,1,1,0,0]
```

---

### 💡 **Hints**
* Use a stack to keep track of indices.
* Traverse the array from the end.

---

### 🚀 Where is this asked?
This problem (Daily Temperatures) is frequently asked in coding interviews at top companies:
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

This problem is used to test stack usage, array traversal, and efficient coding skills for real-world scenarios.
