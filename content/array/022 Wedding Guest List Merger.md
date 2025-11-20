**Difficulty:** Beginner
## 🧩 Problem: "Wedding Guest List Merger"

### **Story**

At a wedding in Jaipur, two families have prepared sorted guest lists. The organizers want to merge both lists into one sorted list, but the first list has extra empty slots (represented by zeros) at the end to accommodate all guests. Can you help the organizers merge the lists in-place?

Your task is to merge the second sorted array into the first sorted array, modifying the first array in-place.

---

### **Example 1**

**Input:**
```typescript
list1 = [1,2,3,0,0,0]
m = 3
list2 = [2,5,6]
n = 3
```
**Output:**
```typescript
[1,2,2,3,5,6]
```

---

### **Example 2**

**Input:**
```typescript
list1 = [1]
m = 1
list2 = []
n = 0
```
**Output:**
```typescript
[1]
```

---

### **Constraints**
* `0 <= m, n <= 200`
* `1 <= m + n <= 200`
* `-10^9 <= list1[i], list2[j] <= 10^9`
* `list1` and `list2` are sorted in non-decreasing order.

---

### **Function Signature (TypeScript)**
```typescript
function weddingGuestListMerger(list1: number[], m: number, list2: number[], n: number): void
```

---

### **Starter Code**
```typescript
function weddingGuestListMerger(list1: number[], m: number, list2: number[], n: number): void {
    // Write your code here
}

// Example
const l1 = [1,2,3,0,0,0];
weddingGuestListMerger(l1, 3, [2,5,6], 3);
console.log(l1); // Expected output: [1,2,2,3,5,6]

const l2 = [1];
weddingGuestListMerger(l2, 1, [], 0);
console.log(l2); // Expected output: [1]
```

---

### 💡 **Hints**
* Start merging from the end to avoid overwriting elements.
* Use pointers for both arrays and fill from the back.
* Handle edge cases when one array is empty.

---

### 🚀 Where is this asked?
This problem (Merge Sorted Array) is frequently asked in coding interviews at top companies:
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

This problem is used to test array merging, edge case handling, and efficient coding skills for real-world scenarios.
