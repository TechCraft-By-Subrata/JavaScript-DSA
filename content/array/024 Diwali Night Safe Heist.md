**Difficulty:** Intermediate
## 🧩 Problem: "Diwali Night Safe Heist"

### **Story**

On Diwali night in Indore, a clever thief named Kabir is planning a heist. The houses on his street have safes with different amounts of money. However, Kabir knows that robbing two adjacent houses will trigger the alarm. Can you help Kabir figure out the maximum amount he can steal without robbing two neighboring houses?

Your task is to find the maximum sum Kabir can rob from the array of house values, without picking two adjacent values.

---

### **Example 1**

**Input:**
```typescript
safes = [1,2,3,1]
```
**Output:**
```typescript
4
```
**Explanation:**
Rob house 1 (2) and house 3 (1): 2 + 1 = 4

---

### **Example 2**

**Input:**
```typescript
safes = [2,7,9,3,1]
```
**Output:**
```typescript
12
```
**Explanation:**
Rob house 1 (7), house 3 (3), and house 5 (1): 7 + 3 + 1 = 11 (but 2 + 9 + 1 = 12 is better)

---

### **Constraints**
* `1 <= safes.length <= 100`
* `0 <= safes[i] <= 4 * 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function diwaliNightSafeHeist(safes: number[]): number
```

---

### **Starter Code**
```typescript
function diwaliNightSafeHeist(safes: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(diwaliNightSafeHeist([1,2,3,1])); // Expected output: 4
console.log(diwaliNightSafeHeist([2,7,9,3,1])); // Expected output: 12
```

---

### 💡 **Hints**
* Use dynamic programming to keep track of the best sum at each house.
* At each house, choose the max between robbing it or skipping it.
* Try to solve in O(n) time and O(1) space.

---

### 🚀 Where is this asked?
This problem (House Robber) is frequently asked in coding interviews at top companies:
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

This problem is used to test dynamic programming, edge case handling, and efficient coding skills for real-world scenarios.
