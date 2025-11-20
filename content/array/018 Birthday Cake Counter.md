**Difficulty:** Beginner
## 🧩 Problem: "Birthday Cake Counter"

### **Story**

In Hyderabad, Rohan is celebrating his birthday with a giant cake divided into slices. Each slice is numbered, and the total number of slices is represented as an array of digits. After blowing out the candles, Rohan wants to add one more slice to the cake. Can you help Rohan update the array to reflect the new total?

Your task is to add one to the number represented by the array of digits and return the updated array.

---

### **Example 1**

**Input:**
```typescript
digits = [1,2,3]
```
**Output:**
```typescript
[1,2,4]
```
**Explanation:**
123 + 1 = 124

---

### **Example 2**

**Input:**
```typescript
digits = [9,9,9]
```
**Output:**
```typescript
[1,0,0,0]
```
**Explanation:**
999 + 1 = 1000

---

### **Constraints**
* `1 <= digits.length <= 100`
* `0 <= digits[i] <= 9`

---

### **Function Signature (TypeScript)**
```typescript
function birthdayCakeCounter(digits: number[]): number[]
```

---

### **Starter Code**
```typescript
function birthdayCakeCounter(digits: number[]): number[] {
    // Write your code here
    return [];
}

// Example
console.log(birthdayCakeCounter([1,2,3])); // Expected output: [1,2,4]
console.log(birthdayCakeCounter([9,9,9])); // Expected output: [1,0,0,0]
```

---

### 💡 **Hints**
* Start from the last digit and handle carry.
* If all digits are 9, add a new digit at the front.
* Use a loop to process each digit from right to left.

---

### 🚀 Where is this asked?
This problem (Plus One) is frequently asked in coding interviews at top companies:
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

This problem is used to test array manipulation, edge case handling, and efficient coding skills for real-world scenarios.
