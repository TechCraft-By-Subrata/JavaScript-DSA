**Difficulty:** Intermediate
## 🧩 Problem: "Next Lucky Draw"

### **Story**

During the annual school fest in Kolkata, Ananya is in charge of the lucky draw. Each ticket has a unique number, and the tickets are arranged in a specific order. After each round, Ananya wants to rearrange the tickets to the next possible order (permutation) that is just greater than the current one, following the rules of the lucky draw. If the current arrangement is the highest possible, she should rearrange the tickets to the lowest possible order.

Your task is to help Ananya find the next lucky draw arrangement for the given ticket numbers.

---

### **Example 1**

**Input:**
```typescript
tickets = [1, 2, 3]
```
**Explanation:**
- The next arrangement is [1, 3, 2].

**Output:**
```typescript
[1, 3, 2]
```

---

### **Example 2**

**Input:**
```typescript
tickets = [3, 2, 1]
```
**Explanation:**
- This is the highest possible arrangement. The next arrangement is the lowest: [1, 2, 3].

**Output:**
```typescript
[1, 2, 3]
```

---

### **Example 3**

**Input:**
```typescript
tickets = [1, 1, 5]
```
**Explanation:**
- The next arrangement is [1, 5, 1].

**Output:**
```typescript
[1, 5, 1]
```

---

### **Constraints**
* `1 <= tickets.length <= 10000`
* `0 <= tickets[i] <= 10000`

---

### **Function Signature (TypeScript)**
```typescript
function nextLuckyDraw(tickets: number[]): number[]
```

---

### **Starter Code**
```typescript
function nextLuckyDraw(tickets: number[]): number[] {
    // Write your code here
    return [];
}

// Example
console.log(nextLuckyDraw([1, 2, 3])); // Expected output: [1, 3, 2]
console.log(nextLuckyDraw([3, 2, 1])); // Expected output: [1, 2, 3]
console.log(nextLuckyDraw([1, 1, 5])); // Expected output: [1, 5, 1]
```

---

### 💡 **Hints**
* Find the first index from the end where tickets[i] < tickets[i+1].
* Swap it with the smallest number greater than it to the right.
* Reverse the part of the array after the swapped index.

---

---

### 🚀 Where is this asked?
This problem (Next Permutation) is popular in coding interviews at top companies:
- Google
- Amazon
- Microsoft
- Flipkart
- Goldman Sachs
- Uber
- Atlassian
- Paytm
- Swiggy
- Zomato

**Relevant Roles:**
- Software Engineer (SDE)
- Data Scientist
- Backend Developer
- Frontend Developer
- Algorithm Engineer
- Technical Lead

This problem is especially important for roles that require strong problem-solving and algorithmic thinking.

Solving it will help you prepare for technical rounds at these companies!
