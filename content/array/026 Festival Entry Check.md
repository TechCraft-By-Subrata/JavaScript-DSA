**Difficulty:** Beginner
## 🧩 Problem: "Festival Entry Check"

### **Story**

At the entrance of the Kolkata Book Festival, every visitor receives a unique entry ticket number. However, the organizers suspect that some tickets might have been duplicated due to a printing error. Can you help the organizers quickly check if any ticket number appears more than once in the list?

Your task is to determine if any number in the array appears at least twice.

---

### **Example 1**

**Input:**
```typescript
tickets = [1,2,3,4,5]
```
**Output:**
```typescript
false
```
**Explanation:**
All ticket numbers are unique.

---

### **Example 2**

**Input:**
```typescript
tickets = [1,2,3,1]
```
**Output:**
```typescript
true
```
**Explanation:**
Ticket number 1 appears twice.

---

### **Constraints**
* `1 <= tickets.length <= 10^5`
* `-10^9 <= tickets[i] <= 10^9`

---

### **Function Signature (TypeScript)**
```typescript
function festivalEntryCheck(tickets: number[]): boolean
```

---

### **Starter Code**
```typescript
function festivalEntryCheck(tickets: number[]): boolean {
    // Write your code here
    return false;
}

// Example
console.log(festivalEntryCheck([1,2,3,4,5])); // Expected output: false
console.log(festivalEntryCheck([1,2,3,1])); // Expected output: true
```

---

### 💡 **Hints**
* Use a set to track seen ticket numbers.
* Return true as soon as a duplicate is found.
* Try to solve in O(n) time and O(n) space.

---

### 🚀 Where is this asked?
This problem (Contains Duplicate) is frequently asked in coding interviews at top companies:
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

This problem is used to test hash set usage, edge case handling, and efficient coding skills for real-world scenarios.
