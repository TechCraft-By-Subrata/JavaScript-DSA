**Difficulty:** Medium
## 🧩 Problem: "Banyan Tree Merge"

### **Story**

In the gardens of Kolkata, two ancient banyan trees are being merged to create a grand centerpiece for the annual festival. Each tree is represented as a binary tree, and the merging process involves adding the values of overlapping nodes. If a node exists in only one tree, it is used as is. Can you help the gardeners merge the trees?

Given two binary trees, merge them by adding the values of overlapping nodes. Return the merged tree.

---

### **Example 1**

**Input:**
```typescript
tree1 = [1,3,2,5]
tree2 = [2,1,3,null,4,null,7]
```
**Output:**
```typescript
[3,4,5,5,4,null,7]
```
**Explanation:**
The merged tree is constructed by adding overlapping nodes.

---

### **Constraints**
* The number of nodes in both trees is in the range `[0, 2000]`.
* `-10^4 <= Node.val <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
class TreeNode {
    val: number;
    left: TreeNode | null;
    right: TreeNode | null;
    constructor(val?: number, left?: TreeNode | null, right?: TreeNode | null) {
        this.val = (val===undefined ? 0 : val)
        this.left = (left===undefined ? null : left)
        this.right = (right===undefined ? null : right)
    }
}

function banyanTreeMerge(tree1: TreeNode | null, tree2: TreeNode | null): TreeNode | null
```

---

### **Starter Code**
```typescript
class TreeNode {
    val: number;
    left: TreeNode | null;
    right: TreeNode | null;
    constructor(val?: number, left?: TreeNode | null, right?: TreeNode | null) {
        this.val = (val===undefined ? 0 : val)
        this.left = (left===undefined ? null : left)
        this.right = (right===undefined ? null : right)
    }
}

function banyanTreeMerge(tree1: TreeNode | null, tree2: TreeNode | null): TreeNode | null {
    // Write your code here
    return null;
}
```

---

### 💡 **Hints**
* Use recursion to merge nodes.
* If a node is null in one tree, use the node from the other tree.

---

### 🚀 Where is this asked?
This problem (Merge Two Binary Trees) is frequently asked in coding interviews at top companies:
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

This problem is used to test recursion, tree traversal, and edge case handling for real-world scenarios.
