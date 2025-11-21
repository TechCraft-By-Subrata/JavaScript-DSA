**Difficulty:** Medium
## 🧩 Problem: "River Pebble Stream"

### **Story**

In Kerala, children play a game by dropping pebbles into a river stream. Each pebble has a value, and the goal is to always know the Kth largest pebble value as new pebbles are added. Can you help them keep track of the Kth largest pebble in the stream?

Design a class that finds the Kth largest element in a stream of numbers. Implement the class with methods to add a new pebble and get the Kth largest pebble value.

---

### **Example 1**

**Input:**
```typescript
k = 3
initialPebbles = [4,5,8,2]
add(3) -> 4
add(5) -> 5
add(10) -> 5
add(9) -> 8
add(4) -> 8
```
**Output:**
```typescript
[4,5,5,8,8]
```
**Explanation:**
After each addition, the Kth largest pebble value is returned.

---

### **Constraints**
* `1 <= k <= 10^4`
* `0 <= initialPebbles.length <= 10^4`
* `-10^4 <= pebble value <= 10^4`

---

### **Function Signature (TypeScript)**
```typescript
class RiverPebbleStream {
    constructor(k: number, initialPebbles: number[])
    add(val: number): number
}
```

---

### **Starter Code**
```typescript
class RiverPebbleStream {
    constructor(k: number, initialPebbles: number[]) {
        // Write your code here
    }
    add(val: number): number {
        // Write your code here
        return 0;
    }
}

// Example
const stream = new RiverPebbleStream(3, [4,5,8,2]);
console.log(stream.add(3)); // Expected output: 4
console.log(stream.add(5)); // Expected output: 5
console.log(stream.add(10)); // Expected output: 5
console.log(stream.add(9)); // Expected output: 8
console.log(stream.add(4)); // Expected output: 8
```

---

### 💡 **Hints**
* Use a min-heap to keep track of the K largest elements.
* Heapify the initial array and maintain the heap size.

---

### 🚀 Where is this asked?
This problem (Kth Largest Element in a Stream) is frequently asked in coding interviews at top companies:
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

This problem is used to test heap usage, stream processing, and efficient coding skills for real-world scenarios.
