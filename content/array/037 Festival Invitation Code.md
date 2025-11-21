**Difficulty:** Beginner
## 🧩 Problem: "Festival Invitation Code"

### **Story**

At the Jaipur Literature Festival, each invitation code is a string of letters. The organizers want to find the first unique character in each code to use as a special identifier. Can you help them find the first character that appears only once in the string?

Your task is to return the index of the first non-repeating character in the string, or -1 if every character repeats.

---

### **Example 1**

**Input:**
```typescript
code = "leetcode"
```
**Output:**
```typescript
0
```
**Explanation:**
'l' is the first unique character.

---

### **Example 2**

**Input:**
```typescript
code = "loveleetcode"
```
**Output:**
```typescript
2
```
**Explanation:**
'v' is the first unique character.

---

### **Example 3**

**Input:**
```typescript
code = "aabb"
```
**Output:**
```typescript
-1
```
**Explanation:**
No unique character.

---

### **Constraints**
* `1 <= code.length <= 10^5`
* `code` consists of only lowercase English letters.

---

### **Function Signature (TypeScript)**
```typescript
function festivalInvitationCode(code: string): number
```

---

### **Starter Code**
```typescript
function festivalInvitationCode(code: string): number {
    // Write your code here
    return -1;
}

// Example
console.log(festivalInvitationCode("leetcode")); // Expected output: 0
console.log(festivalInvitationCode("loveleetcode")); // Expected output: 2
console.log(festivalInvitationCode("aabb")); // Expected output: -1
```

---

### 💡 **Hints**
* Use a hash map to count occurrences of each character.
* Scan the string to find the first character with count 1.
* Try to solve in O(n) time.

---

### 🚀 Where is this asked?
This problem (First Unique Character in a String) is frequently asked in coding interviews at top companies:
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

This problem is used to test hash map usage, string traversal, edge case handling, and efficient coding skills for real-world scenarios.
