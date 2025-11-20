**Difficulty:** Advanced
## 🧩 Problem: "Diwali Code Quartet"

### **Story**

Four cousins—Riya, Aarav, Meera, and Kabir—are celebrating Diwali in Jaipur. Their family has hidden a special Diwali gift, and the secret to unlocking it is a code: the sum of four different numbers from a list of clues must equal a target value. The cousins want to know:

> Can they find **all unique groups of four clues** whose sum equals the target code?

Your task is to help Riya, Aarav, Meera, and Kabir by finding **all unique quadruplets** of clues that sum to the target. Each quadruplet should be listed in ascending order, and the overall list should not contain duplicate quadruplets.

---

### **Example 1**

**Input:**
```typescript
clues = [1, 0, -1, 0, -2, 2]
target = 0
```
**Explanation:**
- The quadruplets that sum to 0 are:
  - [-2, -1, 1, 2]
  - [-2, 0, 0, 2]
  - [-1, 0, 0, 1]

**Output:**
```typescript
[[-2, -1, 1, 2], [-2, 0, 0, 2], [-1, 0, 0, 1]]
```

---

### **Example 2**

**Input:**
```typescript
clues = [2, 2, 2, 2, 2]
target = 8
```
**Explanation:**
- Only one quadruplet: [2, 2, 2, 2]

**Output:**
```typescript
[[2, 2, 2, 2]]
```

---

### **Constraints**
* `4 <= clues.length <= 200`
* `-10^9 <= clues[i] <= 10^9`
* `-10^9 <= target <= 10^9`

---

### **Function Signature (TypeScript)**
```typescript
function diwaliCodeQuartet(clues: number[], target: number): number[][]
```

---

### **Starter Code**
```typescript
function diwaliCodeQuartet(clues: number[], target: number): number[][] {
    // Write your code here
    return [];
}

// Example
console.log(diwaliCodeQuartet([1, 0, -1, 0, -2, 2], 0)); // Expected output: [[-2, -1, 1, 2], [-2, 0, 0, 2], [-1, 0, 0, 1]]
console.log(diwaliCodeQuartet([2, 2, 2, 2, 2], 8)); // Expected output: [[2, 2, 2, 2]]
```

---

### 💡 **Hints**
* Sort the clues first to make it easier to avoid duplicates.
* Use two nested loops to fix the first two numbers, then use two pointers for the remaining two.
* Skip duplicate values to ensure unique quadruplets.

---

### 🚀 Where is this asked?
This problem (4Sum) is frequently asked in coding interviews at top companies:
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

This problem is used to test advanced problem-solving skills, handling complex edge cases, and writing efficient code for challenging scenarios.
