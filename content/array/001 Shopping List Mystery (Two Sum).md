**Difficulty:** Beginner
## 🧩 Problem: "The Shopping List Mystery"

### **Story**

A group of friends, Alex and Jamie, are shopping for a party. They have a list of item prices, and a fixed budget for buying exactly two items. The friends want to know:

> Can they find **two different items** whose prices add up exactly to their budget?

Your task is to help Alex and Jamie by finding the **indices** of the two items whose prices sum to the budget. If there are multiple solutions, return any one pair. Assume there is always exactly one solution.

---

### **Example 1**

**Input:**

```typescript
prices = [7, 11, 15, 2]
budget = 9
```

**Explanation:**
- Alex and Jamie can buy the items at indices 0 and 3 (prices 7 and 2).
- 7 + 2 = 9, which matches their budget.

**Output:**

```typescript
[0, 3]
```

---

### **Example 2**

**Input:**

```typescript
prices = [1, 4, 5, 6]
budget = 10
```

**Explanation:**
- Items at indices 1 and 3 (prices 4 and 6) add up to 10.

**Output:**

```typescript
[1, 3]
```

---

### **Constraints**

* `2 <= prices.length <= 10^4`
* `-10^9 <= prices[i] <= 10^9`
* `-10^9 <= budget <= 10^9`
* There is **exactly one solution**.

---

### **Function Signature (TypeScript)**

```typescript
function shoppingListMystery(prices: number[], budget: number): [number, number]
```

---

### **Starter Code**

```typescript
function shoppingListMystery(prices: number[], budget: number): [number, number] {
    // Write your code here
    return [0, 0];
}

// Example
console.log(shoppingListMystery([7, 11, 15, 2], 9)); // Expected output: [0, 3]
console.log(shoppingListMystery([1, 4, 5, 6], 10)); // Expected output: [1, 3]
```

---

### 💡 **Hints**

* Use a hash map to store prices you’ve seen so far.
* For each price, check if (budget - price) is already in the map.
* Return the indices as soon as you find a match.

---

### 🚀 Where is this asked?
This problem (Two Sum) is extremely popular in coding interviews at top companies:
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

**Relevant Roles:**
- Software Engineer (SDE)
- Backend Developer
- Frontend Developer
- Data Scientist
- Algorithm Engineer

This problem is a classic warm-up for technical interviews and is often used to test basic problem-solving and coding skills.
