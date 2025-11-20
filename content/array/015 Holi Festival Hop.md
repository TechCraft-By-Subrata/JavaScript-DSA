**Difficulty:** Intermediate
## 🧩 Problem: "Holi Festival Hop"

### **Story**

During the Holi festival in Mathura, Anaya and her friends are playing a game where they must hop across a series of colored mats laid out in a line. Each mat has a number indicating the maximum distance they can jump forward from that mat. Anaya wants to know if she can reach the last mat starting from the first one.

Your task is to help Anaya determine if it's possible to reach the last mat by hopping according to the numbers on each mat.

---

### **Example 1**

**Input:**
```typescript
mats = [2,3,1,1,4]
```
**Output:**
```typescript
true
```
**Explanation:**
Anaya can hop from mat 0 to mat 1 (2 steps), then from mat 1 to mat 4 (3 steps).

---

### **Example 2**

**Input:**
```typescript
mats = [3,2,1,0,4]
```
**Output:**
```typescript
false
```
**Explanation:**
Anaya gets stuck at mat 3 and cannot reach the last mat.

---

### **Constraints**
* `1 <= mats.length <= 10^4`
* `0 <= mats[i] <= 10^5`

---

### **Function Signature (TypeScript)**
```typescript
function holiFestivalHop(mats: number[]): boolean
```

---

### **Starter Code**
```typescript
function holiFestivalHop(mats: number[]): boolean {
    // Write your code here
    return false;
}

// Example
console.log(holiFestivalHop([2,3,1,1,4])); // Expected output: true
console.log(holiFestivalHop([3,2,1,0,4])); // Expected output: false
```

---

### 💡 **Hints**
* Track the farthest mat you can reach at each step.
* If you reach or pass the last mat, return true.
* If you get stuck before the last mat, return false.

---

### 🚀 Where is this asked?
This problem (Jump Game) is frequently asked in coding interviews at top companies:
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

This problem is used to test greedy algorithms, edge case handling, and efficient coding skills for real-world scenarios.
