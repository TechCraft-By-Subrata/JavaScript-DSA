**Difficulty:** Intermediate
## 🧩 Problem: "Search in Rotated Sorted Array"

### **Story**

During the annual Kolkata Book Fair, Priya is searching for a rare book in a long row of stalls. The stalls are arranged in a peculiar way: the order of books is sorted, but at some unknown point, the sequence is rotated. Priya knows the name of the book she wants (represented as a number), and she wants to find the exact stall (index) where it is located.

Your task is to help Priya by finding the index of the target book in the rotated sorted array. If the book is not present, return -1.

---

### **Example 1**

**Input:**
```typescript
books = [4,5,6,7,0,1,2]
target = 0
```
**Output:**
```typescript
4
```

---

### **Example 2**

**Input:**
```typescript
books = [4,5,6,7,0,1,2]
target = 3
```
**Output:**
```typescript
-1
```

---

### **Constraints**
* `1 <= books.length <= 5000`
* `-10^4 <= books[i] <= 10^4`
* All values of books are unique.
* `-10^4 <= target <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
function searchInRotatedSortedArray(books: number[], target: number): number
```

---

### **Starter Code**
```typescript
function searchInRotatedSortedArray(books: number[], target: number): number {
    // Write your code here
    return -1;
}

// Example
console.log(searchInRotatedSortedArray([4,5,6,7,0,1,2], 0)); // Expected output: 4
console.log(searchInRotatedSortedArray([4,5,6,7,0,1,2], 3)); // Expected output: -1
```

---

### 💡 **Hints**
* Use binary search to achieve O(log n) time complexity.
* Check which half of the array is sorted at each step.
* Adjust search boundaries based on the sorted half.

---

### 🚀 Where is this asked?
This problem (Search in Rotated Sorted Array) is frequently asked in coding interviews at top companies:
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
