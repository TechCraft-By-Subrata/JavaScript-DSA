**Difficulty:** Advanced
## 🧩 Problem: "Fest Pass Duplicate Hunt"

### **Story**

At the Lucknow Literature Fest, every attendee receives a unique pass number. However, due to a printing error, one pass number was accidentally duplicated. The organizers want to quickly find the duplicate pass number to prevent confusion. Can you help them identify the duplicate?

Your task is to find the single duplicate number in the array of pass numbers.

---

### **Example 1**

**Input:**
```typescript
passes = [1,3,4,2,2]
```
**Output:**
```typescript
2
```
**Explanation:**
Pass number 2 is duplicated.

---

### **Example 2**

**Input:**
```typescript
passes = [3,1,3,4,2]
```
**Output:**
```typescript
3
```
**Explanation:**
Pass number 3 is duplicated.

---

### **Constraints**
* `1 <= passes.length <= 10^5`
* `1 <= passes[i] <= passes.length - 1`
* There is only one repeated number, but it may be repeated more than once.

---

### **Function Signature (TypeScript)**
```typescript
function festPassDuplicateHunt(passes: number[]): number
```

---

### **Starter Code**
```typescript
function festPassDuplicateHunt(passes: number[]): number {
    // Write your code here
    return -1;
}

// Example
console.log(festPassDuplicateHunt([1,3,4,2,2])); // Expected output: 2
console.log(festPassDuplicateHunt([3,1,3,4,2])); // Expected output: 3
```

---

### 💡 **Hints**
* Use Floyd's Tortoise and Hare (cycle detection) algorithm for O(n) time and O(1) space.
* Alternatively, use a set to track seen numbers (O(n) space).
* The array cannot be modified.

---

### 🚀 Where is this asked?
This problem (Find the Duplicate Number) is frequently asked in coding interviews at top companies:
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

This problem is used to test cycle detection, hash set usage, edge case handling, and efficient coding skills for real-world scenarios.
