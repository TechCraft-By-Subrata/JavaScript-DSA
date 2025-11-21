## 🧩 Problem: "Festival Guest List Cleanup"
**Difficulty:** Beginner

### **Story**

During the Diwali festival, Rohan is helping his friend Priya organize a guest list for their family party. The guest list is sorted by phone number, but due to a technical glitch, some phone numbers appear multiple times in a row. Priya wants the list to have only one entry for each guest, keeping the order, and all unique phone numbers should be at the front of the list. The extra repeated numbers can be ignored.

Your task is to help Rohan and Priya clean up the guest list so that each phone number appears only once, and return the total number of unique guests. The cleaned list should have all unique numbers at the beginning, and you don't need to worry about the leftover repeated numbers after that.

---

### **Example 1**

**Input:**
```typescript
guestList = [9999943210, 9999943210, 9999943222, 9999943222, 9999943233]
```
**Explanation:**
- Unique guests: [9999943210, 9999943222, 9999943233]
- The first three entries of the list should be these numbers.
- Return 3 (the count of unique guests).

**Output:**
```typescript
3
```

---

### **Example 2**

**Input:**
```typescript
guestList = [9123456789, 9123456789, 9123456789]
```
**Explanation:**
- Only one unique guest: [9123456789]
- Return 1.

**Output:**
```typescript
1
```

---

### **Constraints**
* `1 <= guestList.length <= 10^4`
* `6000000000 <= guestList[i] <= 9999999999` (valid Indian mobile numbers)
* The list is sorted in non-decreasing order.

---

### **Function Signature (TypeScript)**
```typescript
function festivalGuestListCleanup(guestList: number[]): number
```

---

### **Starter Code**
```typescript
function festivalGuestListCleanup(guestList: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(festivalGuestListCleanup([9999943210, 9999943210, 9999943222, 9999943222, 9999943233])); // Expected output: 3
console.log(festivalGuestListCleanup([9123456789, 9123456789, 9123456789])); // Expected output: 1
```

---

### 💡 **Hints**
* Use two pointers to overwrite duplicates in the array.
* Only keep the first occurrence of each phone number.
* Return the count of unique guests.

---

### 🚀 Where is this asked?
This problem (Remove Duplicates from Sorted Array) is frequently asked in coding interviews at top companies:
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

This problem is used to test two-pointer technique, edge case handling, and efficient coding skills for real-world scenarios.
