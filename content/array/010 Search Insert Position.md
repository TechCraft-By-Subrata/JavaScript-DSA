**Difficulty:** Beginner
## 🧩 Problem: "Search Insert Position"

### **Story**

At the Bengaluru Science Fair, Aarav is helping his younger sister, Riya, organize her collection of science books. The books are arranged in increasing order by their ID numbers. Whenever Riya gets a new book, she wants to know where to insert it so that the order remains sorted. Aarav needs to quickly find the correct position for any new book ID.

Your task is to help Aarav by finding the index where the new book should be inserted. If the book already exists, return its index.

---

### **Example 1**

**Input:**
```typescript
books = [1,3,5,6]
target = 5
```
**Output:**
```typescript
2
```

---

### **Example 2**

**Input:**
```typescript
books = [1,3,5,6]
target = 2
```
**Output:**
```typescript
1
```

---

### **Constraints**
* `1 <= books.length <= 10^4`
* `-10^4 <= books[i] <= 10^4`
* `books` is sorted in ascending order.
* `-10^4 <= target <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function searchInsertPosition(books: number[], target: number): number
```

---

### **Starter Code**
```typescript
function searchInsertPosition(books: number[], target: number): number {
    // Write your code here
    return 0;
}

// Example
console.log(searchInsertPosition([1,3,5,6], 5)); // Expected output: 2
console.log(searchInsertPosition([1,3,5,6], 2)); // Expected output: 1
```

---

### 💡 **Hints**
* Use binary search for O(log n) time complexity.
* If the target is not found, return the index where it would be inserted.
* Check edge cases for smallest and largest values.

---

### 🚀 Where is this asked?
This problem (Search Insert Position) is frequently asked in coding interviews at top companies:
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

This problem is used to test binary search skills, handling edge cases, and writing efficient code for real-world scenarios.
