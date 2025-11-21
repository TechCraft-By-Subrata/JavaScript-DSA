**Difficulty:** Advanced
## 🧩 Problem: "Festival Entry Check III"

### **Story**

At the Bengaluru Tech Expo, every visitor receives a ticket number as they enter. The organizers want to ensure that no ticket number is used more than once within a short time window, and that the ticket numbers are not too close in value to each other, to prevent fraud. Given a list of ticket numbers, and two numbers k and t, can you help the organizers check if any two ticket numbers appear within k entries of each other and have a difference of at most t?

Your task is to determine if there are two distinct indices i and j in the array such that:
- `abs(tickets[i] - tickets[j]) <= t`
- `abs(i - j) <= k`

---

### **Example 1**

**Input:**
```typescript
tickets = [1,2,3,1]
k = 3
t = 0
```
**Output:**
```typescript
true
```
**Explanation:**
Ticket number 1 appears twice within 3 entries and their difference is 0.

---

### **Example 2**

**Input:**
```typescript
tickets = [1,0,1,1]
k = 1
t = 2
```
**Output:**
```typescript
true
```
**Explanation:**
Ticket numbers 1 and 0 are within 1 entry and their difference is 1.

---

### **Example 3**

**Input:**
```typescript
tickets = [1,5,9,1,5,9]
k = 2
t = 3
```
**Output:**
```typescript
false
```
**Explanation:**
No ticket numbers meet both conditions.

---

### **Constraints**
* `1 <= tickets.length <= 2 * 10^4`
* `-2^{31} <= tickets[i] <= 2^{31} - 1`
* `1 <= k <= 10^4`
* `0 <= t <= 2^{31} - 1`

---

### **Function Signature (TypeScript)**
```typescript
function festivalEntryCheckIII(tickets: number[], k: number, t: number): boolean
```

---

### **Starter Code**
```typescript
function festivalEntryCheckIII(tickets: number[], k: number, t: number): boolean {
    // Write your code here
    return false;
}

// Example
console.log(festivalEntryCheckIII([1,2,3,1], 3, 0)); // Expected output: true
console.log(festivalEntryCheckIII([1,0,1,1], 1, 2)); // Expected output: true
console.log(festivalEntryCheckIII([1,5,9,1,5,9], 2, 3)); // Expected output: false
```

---

### 💡 **Hints**
* Use a balanced BST or bucket sort to efficiently check for nearby duplicates.
* Maintain a sliding window of size k.
* Try to solve in O(n) time and O(k) space.

---

### 🚀 Where is this asked?
This problem (Contains Duplicate III) is frequently asked in coding interviews at top companies:
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

This problem is used to test advanced hash map and BST usage, sliding window, edge case handling, and efficient coding skills for real-world scenarios.
