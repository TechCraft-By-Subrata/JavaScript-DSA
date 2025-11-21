
**Difficulty:** Beginner
## 🧩 Problem: "Grocery Bazaar Challenge"

### **Story**

Priya and Aman are shopping together at a local bazaar in Pune for a family get-together. They have a list of item prices, and a fixed budget to buy exactly two items. Priya wants to buy samosas and Aman wants to buy rasgullas, but they must make sure the total cost does not exceed their budget.

> Can Priya and Aman find **two different items** whose prices add up exactly to their budget?

Your task is to help Priya and Aman by finding the **indices** of the two items whose prices sum to the budget. If there are multiple solutions, return any one pair. Assume there is always exactly one solution.

---

### **Example 1**

**Input:**
```typescript
prices = [15, 20, 35, 5]
budget = 20
```
**Explanation:**
- Priya and Aman can buy the items at indices 0 and 3 (prices 15 and 5).
- 15 + 5 = 20, which matches their budget.

**Output:**
```typescript
[0, 3]
```

---

### **Example 2**

**Input:**
```typescript
prices = [10, 25, 30, 40]
budget = 55
```
**Explanation:**
- Items at indices 1 and 2 (prices 25 and 30) add up to 55.

**Output:**
```typescript
[1, 2]
```

---

### **Constraints**
* `2 <= prices.length <= 10^4`
* `1 <= prices[i] <= 10^5`
* `1 <= budget <= 2*10^5`
* There is **exactly one solution**.

---

### **Function Signature (TypeScript)**
```typescript
function groceryBazaarChallenge(prices: number[], budget: number): [number, number]
```

---

### **Starter Code**
```typescript
function groceryBazaarChallenge(prices: number[], budget: number): [number, number] {
    // Write your code here
    return [0, 0];
}

// Example
console.log(groceryBazaarChallenge([15, 20, 35, 5], 20)); // Expected output: [0, 3]
console.log(groceryBazaarChallenge([10, 25, 30, 40], 55)); // Expected output: [1, 2]
```

---

### 💡 **Hints**
* Use a hash map to store prices you’ve seen so far.
* For each price, check if (budget - price) is already in the map.
* Return the indices as soon as you find a match.

---

### 🚀 Where is this asked?
This problem (Two Sum) is frequently asked in coding interviews at top companies:
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
- Frontend Developer (JavaScript/TypeScript)
- Backend Developer
- Full Stack Developer
- Software Engineer (Entry to Mid-level)
- Data Analyst/Engineer (for algorithmic thinking)
- Technical Interview Candidate

This problem is used to test hash map usage, edge case handling, and efficient coding skills for real-world scenarios.
