**Difficulty:** Advanced
## 🧩 Problem: "Treasure Hunt Word Search"

### **Story**

In the ancient city of Varanasi, a group of friends is participating in a treasure hunt. The clues are hidden in a grid of letters, and each clue is a word that can be formed by connecting adjacent letters horizontally or vertically. Each letter cell can be used only once per word. Can you help the friends find if a given word exists in the grid?

Your task is to determine if the target word exists in the grid by connecting adjacent letters.

---

### **Example 1**

**Input:**
```typescript
board = [
  ['A','B','C','E'],
  ['S','F','C','S'],
  ['A','D','E','E']
]
word = "ABCCED"
```
**Output:**
```typescript
true
```

---

### **Example 2**

**Input:**
```typescript
board = [
  ['A','B','C','E'],
  ['S','F','C','S'],
  ['A','D','E','E']
]
word = "SEE"
```
**Output:**
```typescript
true
```

---

### **Example 3**

**Input:**
```typescript
board = [
  ['A','B','C','E'],
  ['S','F','C','S'],
  ['A','D','E','E']
]
word = "ABCB"
```
**Output:**
```typescript
false
```

---

### **Constraints**
* `1 <= board.length, board[i].length <= 6`
* `1 <= word.length <= 15`
* `board` and `word` consist of only uppercase English letters.

---

### **Function Signature (TypeScript)**
```typescript
function treasureHuntWordSearch(board: string[][], word: string): boolean
```

---

### **Starter Code**
```typescript
function treasureHuntWordSearch(board: string[][], word: string): boolean {
    // Write your code here
    return false;
}

// Example
console.log(treasureHuntWordSearch([
  ['A','B','C','E'],
  ['S','F','C','S'],
  ['A','D','E','E']
], "ABCCED")); // Expected output: true
console.log(treasureHuntWordSearch([
  ['A','B','C','E'],
  ['S','F','C','S'],
  ['A','D','E','E']
], "SEE")); // Expected output: true
console.log(treasureHuntWordSearch([
  ['A','B','C','E'],
  ['S','F','C','S'],
  ['A','D','E','E']
], "ABCB")); // Expected output: false
```

---

### 💡 **Hints**
* Use backtracking to explore all possible paths.
* Mark visited cells to avoid reusing them in the same word.
* Prune paths early if the current cell does not match the next letter.

---

### 🚀 Where is this asked?
This problem (Word Search) is frequently asked in coding interviews at top companies:
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

This problem is used to test backtracking, matrix traversal, edge case handling, and efficient coding skills for real-world scenarios.
