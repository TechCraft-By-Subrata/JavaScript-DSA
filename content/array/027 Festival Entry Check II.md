**Difficulty:** Beginner
## 🧩 Problem: "Festival Entry Check II"

### **Story**

At the Mumbai Food Carnival, every visitor receives a ticket number as they enter. The organizers want to ensure that no ticket number is used more than once within a short time window, to prevent fraud. Given a list of ticket numbers and a number k, can you help the organizers check if any ticket number appears at least twice within k entries of each other?

Your task is to determine if any number in the array appears at least twice within k indices of each other.

---

### **Example 1**

**Input:**
```typescript
tickets = [1,2,3,1]
k = 3
```
**Output:**
```typescript
true
```
**Explanation:**
Ticket number 1 appears twice within 3 entries.

---

### **Example 2**

**Input:**
```typescript
tickets = [1,0,1,1]
k = 1
```
**Output:**
```typescript
true
```
**Explanation:**
Ticket number 1 appears twice within 1 entry.

---

### **Example 3**

**Input:**
```typescript
tickets = [1,2,3,1,2,3]
k = 2
```
**Output:**
```typescript
false
```
**Explanation:**
No ticket number appears twice within 2 entries.

---

### **Constraints**
* `1 <= tickets.length <= 10^5`
* `-10^9 <= tickets[i] <= 10^9`
* `1 <= k <= 10^5`

---

### **Function Signature (TypeScript)**
```typescript
function festivalEntryCheckII(tickets: number[], k: number): boolean
```

---

### **Starter Code**
```typescript
function festivalEntryCheckII(tickets: number[], k: number): boolean {
    // Write your code here
    return false;
}

// Example
console.log(festivalEntryCheckII([1,2,3,1], 3)); // Expected output: true
console.log(festivalEntryCheckII([1,0,1,1], 1)); // Expected output: true
console.log(festivalEntryCheckII([1,2,3,1,2,3], 2)); // Expected output: false
```

---

### 💡 **Hints**
* Use a hash map to track the last index of each ticket number.
* Check the distance between indices when a duplicate is found.
* Try to solve in O(n) time and O(n) space.

---

### 🚀 Where is this asked?
This problem (Contains Duplicate II) is frequently asked in coding interviews at top companies:
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

This problem is used to test hash map usage, edge case handling, and efficient coding skills for real-world scenarios.
