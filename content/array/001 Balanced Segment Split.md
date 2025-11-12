
## 🧩 Problem: "Balanced Segment Split"

### **Problem Description**

You are given an array of integers `nums`.
Your task is to find the **number of ways** to split the array into **two non-empty contiguous parts** such that:

* The **sum of unique elements** in the left part equals the **sum of unique elements** in the right part.

Return the **count of all such possible split points**.

---

### **Example 1**

**Input:**

```typescript
nums = [2, 3, 3, 2, 4, 5]
```

**Explanation:**

All possible splits:

| Split Index | Left Part       | Right Part      | Unique Sum Left | Unique Sum Right | Valid? |
| ----------- | --------------- | --------------- | --------------- | ---------------- | ------ |
| 1           | [2]             | [3, 3, 2, 4, 5] | 2               | 14               | ❌      |
| 2           | [2, 3]          | [3, 2, 4, 5]    | 5               | 14               | ❌      |
| 3           | [2, 3, 3]       | [2, 4, 5]       | 5               | 11               | ❌      |
| 4           | [2, 3, 3, 2]    | [4, 5]          | 5               | 9                | ❌      |
| 5           | [2, 3, 3, 2, 4] | [5]             | 9               | 5                | ❌      |

✅ **No valid split**, so output is `0`.

**Output:**

```typescript
0
```

---

### **Example 2**

**Input:**

```typescript
nums = [1, 2, 3, 1, 2]
```

**Explanation:**

| Split Index | Left Part | Right Part | Unique Sum Left | Unique Sum Right | Valid? |
| ----------- | --------- | ---------- | --------------- | ---------------- | ------ |
| 1           | [1]       | [2,3,1,2]  | 1               | 6                | ❌      |
| 2           | [1,2]     | [3,1,2]    | 3               | 6                | ❌      |
| 3           | [1,2,3]   | [1,2]      | 6               | 3                | ❌      |
| 4           | [1,2,3,1] | [2]        | 6               | 2                | ❌      |

✅ **No valid split**, so output is `0`.

**Output:**

```typescript
0
```

---

### **Example 3**

**Input:**

```typescript
nums = [1, 2, 2, 1, 3, 3]
```

**Explanation:**

| Split Index | Left Part   | Right Part  | Unique Sum Left | Unique Sum Right | Valid? |
| ----------- | ----------- | ----------- | --------------- | ---------------- | ------ |
| 1           | [1]         | [2,2,1,3,3] | 1               | 6                | ❌      |
| 2           | [1,2]       | [2,1,3,3]   | 3               | 6                | ❌      |
| 3           | [1,2,2]     | [1,3,3]     | 3               | 4                | ❌      |
| 4           | [1,2,2,1]   | [3,3]       | 3               | 3                | ✅      |
| 5           | [1,2,2,1,3] | [3]         | 6               | 3                | ❌      |

✅ Only **1 valid split** (index = 4).

**Output:**

```typescript
1
```

---

### **Constraints**

* `1 <= nums.length <= 10^5`
* `-10^4 <= nums[i] <= 10^4`

---

### **Follow-up**

Can you solve this in **O(n)** time and **O(n)** space using prefix and suffix maps?

---

### **Function Signature (TypeScript)**

```typescript
function countBalancedSplits(nums: number[]): number
```

---

### **Starter Code**

```typescript
function countBalancedSplits(nums: number[]): number {
    // Write your code here
    return 0;
}

// Example
console.log(countBalancedSplits([1, 2, 2, 1, 3, 3])); // Expected output: 1
```

---

### 💡 **Hints**

* Use two hash maps: one for prefix unique sums and one for suffix unique sums.
* Iterate from left to right updating the prefix, and from right to left updating the suffix.
* Compare prefix sum and suffix sum at each possible split.

---


---

## Explanation — What we are solving

We need to count the number of ways to split an array `nums` into two non-empty contiguous parts *such that the sum of unique elements in the left part equals the sum of unique elements in the right part.*

Unique-sum example: for subarray `[1,2,2,1,3]`, the set of unique elements is `{1,2,3}` and its sum is `1+2+3 = 6`.

A split point is between indices `i` and `i+1`. For `n` elements there are `n-1` possible splits.

---

## 1) Brute-force approach (beginner friendly)

### Idea (book-style):

1. Iterate every possible split point `i` from `1` to `n-1`.
2. For each split, build a `Set` for the left part and compute sum of its elements.
3. Build another `Set` for the right part and compute its unique-sum.
4. If the two sums are equal, increment answer.

This is simple and very explicit: you directly compute the sums for each split. But it repeats work — each split recomputes sets over subarrays again — hence O(n²) in time for typical inputs. This is fine for small arrays or to confirm correctness before optimizing.

---

## 2) Optimal O(n) approach

### Idea:

We avoid recomputing sets for each split by precomputing:

* `prefixUniqueSum[i]` = sum of unique elements in `nums[0..i]` (inclusive)
* `suffixUniqueSum[i]` = sum of unique elements in `nums[i..n-1]` (inclusive)

Then a split between `i` and `i+1` is valid if `prefixUniqueSum[i] === suffixUniqueSum[i+1]`.

How to compute prefix/suffix arrays in O(n):

* For prefix: traverse left → right keeping a `Set` of seen numbers and a running `sum`. When you encounter a new number, add it to `sum`.
* For suffix: traverse right → left similarly.

This makes the time O(n) and space O(n) (for the two arrays and the temporary sets).

---

## Full TypeScript code (both implementations + test harness)

Save as e.g. `balanced_splits_both.ts` and run:

`npx ts-node balanced_splits_both.ts`

```typescript
// balanced_splits_both.ts
// Run with: npx ts-node balanced_splits_both.ts
// Or compile: tsc balanced_splits_both.ts && node balanced_splits_both.js

type TestCase = {
  id: number;
  name: string;
  input: number[];
  expected: number;
};

/* ============================
   BRUTE FORCE IMPLEMENTATION
   (beginner friendly)
   ============================ */

/**
 * Brute force approach (O(n^2) time, O(n) extra per split due to building sets)
 * For each split, construct sets of left and right subarrays and compare sums.
 */
function countBalancedSplitsBruteForce(nums: number[]): number {
  const n = nums.length;
  if (n < 2) return 0;
  let ans = 0;

  for (let split = 1; split <= n - 1; split++) {
    // left: nums[0..split-1], right: nums[split..n-1]
    const leftSet = new Set<number>();
    const rightSet = new Set<number>();
    for (let i = 0; i < split; i++) leftSet.add(nums[i]);
    for (let i = split; i < n; i++) rightSet.add(nums[i]);

    let leftSum = 0;
    for (const v of leftSet) leftSum += v;
    let rightSum = 0;
    for (const v of rightSet) rightSum += v;

    if (leftSum === rightSum) ans++;
  }

  return ans;
}

/* ============================
   OPTIMAL O(n) IMPLEMENTATION
   ============================ */

/**
 * Optimal approach O(n) time, O(n) space:
 * Precompute prefixUniqueSum and suffixUniqueSum arrays using sets while scanning once each direction.
 */
function countBalancedSplitsOptimal(nums: number[]): number {
  const n = nums.length;
  if (n < 2) return 0;

  const prefixUniqueSum: number[] = new Array(n).fill(0);
  const suffixUniqueSum: number[] = new Array(n).fill(0);

  // Build prefixUniqueSum
  const seenPrefix = new Set<number>();
  let runningPrefixSum = 0;
  for (let i = 0; i < n; i++) {
    const v = nums[i];
    if (!seenPrefix.has(v)) {
      seenPrefix.add(v);
      runningPrefixSum += v;
    }
    prefixUniqueSum[i] = runningPrefixSum;
  }

  // Build suffixUniqueSum
  const seenSuffix = new Set<number>();
  let runningSuffixSum = 0;
  for (let i = n - 1; i >= 0; i--) {
    const v = nums[i];
    if (!seenSuffix.has(v)) {
      seenSuffix.add(v);
      runningSuffixSum += v;
    }
    suffixUniqueSum[i] = runningSuffixSum;
  }

  // Compare at each split between i and i+1
  let ans = 0;
  for (let i = 0; i <= n - 2; i++) {
    if (prefixUniqueSum[i] === suffixUniqueSum[i + 1]) ans++;
  }
  return ans;
}

/* ============================
   SELECT MODE: "bruteforce" or "optimal"
   (Switch the below variable to choose which function the harness runs)
   ============================ */

const MODE: "bruteforce" | "optimal" = "optimal";

/* ============================
   TEST HARNESS (unchanged)
   ============================ */

const curatedTests: TestCase[] = [
  { id: 1,  name: "Length 1 (no split)", input: [7], expected: 0 },
  { id: 2,  name: "Length 2, same elements", input: [5,5], expected: 1 },
  { id: 3,  name: "Length 2, different elements", input: [1,2], expected: 0 },
  { id: 4,  name: "All identical elements", input: [2,2,2,2], expected: 3 },
  { id: 5,  name: "Mixed with no valid split", input: [2,3,3,2,4,5], expected: 0 },
  { id: 6,  name: "One valid split", input: [1,2,2,1,3,3], expected: 1 },
  { id: 7,  name: "Increasing uniques", input: [1,2,3,4], expected: 0 },
  { id: 8,  name: "Zeros and negatives", input: [0,-1,1], expected: 1 },
  { id: 9,  name: "Alternating +1 -1", input: [1,-1,1,-1], expected: 1 },
  { id:10,  name: "Large absolute values", input: [10000, -10000, 10000], expected: 0 },
  { id:11,  name: "Repeats then unique tail", input: [3,3,4,5], expected: 0 },
  { id:12,  name: "Symmetric repeats", input: [1,2,1,2], expected: 1 },
  { id:13,  name: "Complex duplicates", input: [1,1,2,3,2,1], expected: 0 },
  { id:14,  name: "Constructed equal unique sums", input: [1,2,3,4,2], expected: 1 },
  { id:15,  name: "Repeated blocks many valid splits", input: [1,2,1,2,1,2], expected: 3 },
  { id:16,  name: "Unique sums equal mid", input: [1,4,3,2], expected: 1 },
  { id:17,  name: "All negatives alternating", input: [-1,-2,-1,-2], expected: 1 },
  { id:18,  name: "Mix producing 2 valid splits", input: [5,1,5,1,5], expected: 2 },
  { id:19,  name: "Plateau then unique", input: [8,8,8,9], expected: 0 },
  { id:20,  name: "Long no-split", input: [1,1,1,2,2,3,3,4,4,5], expected: 0 },
  { id:21,  name: "Alt pattern large", input: [2,3,2,3,2,3,2], expected: 4 },
  { id:22,  name: "Match later", input: [6,7,6,7,6,8], expected: 2 },
  { id:23,  name: "Empty array", input: [], expected: 0 },
  { id:24,  name: "Edge values duplicates", input: [10000,10000,-10000,-10000,10000], expected: 2 },
  { id:25,  name: "Varied one valid split", input: [1,2,3,1,5,6], expected: 0 },
  { id:26,  name: "Tricky constructed", input: [1,2,4,3,4], expected: 1 },
];

const tests = curatedTests;

function computeUniqueSum(arr: number[]): number {
  const set = new Set<number>();
  for (const v of arr) set.add(v);
  let s = 0;
  for (const v of set) s += v;
  return s;
}

function runTests() {
  const func = MODE === "optimal" ? countBalancedSplitsOptimal : countBalancedSplitsBruteForce;
  console.log(`Running tests in MODE="${MODE}" using function: ${func.name}\n`);

  const results: { id: number; name: string; passed: boolean; input: number[]; expected: number; actual: number | string }[] = [];
  for (const tc of tests) {
    let actual: number | string;
    try {
      const out = func(tc.input);
      actual = out;
      const passed = out === tc.expected;
      results.push({ id: tc.id, name: tc.name, passed, input: tc.input, expected: tc.expected, actual: out });
    } catch (err: any) {
      actual = `ERROR: ${err && err.message ? err.message : String(err)}`;
      results.push({ id: tc.id, name: tc.name, passed: false, input: tc.input, expected: tc.expected, actual });
    }
  }

  // Summary
  const passedCount = results.filter(r => r.passed).length;
  const failed = results.filter(r => !r.passed);

  console.log("===========================================");
  console.log(`Balanced Segment Split — Test Run`);
  console.log(`Total tests: ${tests.length}`);
  console.log(`Passed: ${passedCount}`);
  console.log(`Failed: ${failed.length}`);
  console.log("===========================================\n");

  for (const r of results) {
    const mark = r.passed ? "✅ PASS" : "❌ FAIL";
    console.log(`${mark} [#${r.id}] ${r.name}`);
    if (!r.passed) {
      console.log(`   Input: ${JSON.stringify(r.input)}`);
      console.log(`   Expected: ${r.expected}`);
      console.log(`   Actual: ${r.actual}`);
      if (String(r.actual).startsWith("ERROR")) {
        console.log("   (Your function threw an error)");
      } else {
        // Show per-split debug (prefix/suffix unique sums) for debugging
        const arr = r.input;
        if (arr.length >= 2) {
          console.log("   Debug splits (prefixUniqueSum -> suffixUniqueSum):");
          // compute prefix/suffix unique sums for display
          const pre: number[] = [];
          const suf: number[] = [];
          const sset = new Set<number>();
          let ssum = 0;
          for (let i = 0; i < arr.length; i++) {
            if (!sset.has(arr[i])) {
              sset.add(arr[i]);
              ssum += arr[i];
            }
            pre[i] = ssum;
          }
          sset.clear();
          ssum = 0;
          for (let i = arr.length - 1; i >= 0; i--) {
            if (!sset.has(arr[i])) {
              sset.add(arr[i]);
              ssum += arr[i];
            }
            suf[i] = ssum;
          }
          for (let i = 1; i <= arr.length - 1; i++) {
            console.log(`     split@${i}: ${pre[i-1]} -> ${suf[i]} (left=${JSON.stringify(arr.slice(0,i))}, right=${JSON.stringify(arr.slice(i))})`);
          }
        }
      }
      console.log("");
    }
  }

  if (failed.length === 0) {
    console.log("🎉 All test cases passed. Great job!");
  } else {
    console.log(`\nFix the failing tests above. After adjusting your implementation, re-run the file to verify.`);
  }
}

runTests();
```

---

## Notes & Tips

* The **brute-force** function is great to read and reason about. If you are learning, type it out and run it on small inputs so you can step through the logic.
* The **optimal** function is simple once you understand prefix/suffix accumulation. It avoids re-scanning subarrays for each split.
* Both implementations handle negative numbers correctly because sums simply add negatives and sets treat values by identity.
* If you want, I can:

  * Convert this harness to a **Jest** or **Mocha** test suite.
  * Add **randomized property tests** to further validate correctness.
  * Produce a **line-by-line walkthrough** (with small arrays) showing how `prefixUniqueSum` and `suffixUniqueSum` arrays are built.

Want me to switch the `MODE` variable to `"bruteforce"` and re-run the outputs here (showing sample test-run results), or would you like the code converted into a Jest suite?
