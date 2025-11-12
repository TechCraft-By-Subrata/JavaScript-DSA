## 🧩 Problem: "Maximum Subarray Product with K Removals"

### **Problem Description**

You are given an array of integers `nums` and an integer `k`.

Your task is to find the **maximum product** of a contiguous subarray after removing **at most k elements** from it.

* You can remove any elements from the subarray (not necessarily contiguous removals).
* After removal, the remaining elements must form a contiguous sequence from the original subarray.
* The subarray must have at least **one element** remaining after removals.
* If all possible products are negative and you must return a value, return the maximum (least negative) product.

Return the **maximum product** possible.

---

### **Example 1**

**Input:**

```typescript
nums = [2, -3, -4, 5]
k = 1
```

**Explanation:**

Consider subarray `[2, -3, -4, 5]`:
- Remove `-3`: product = `2 × (-4) × 5 = -40`
- Remove `-4`: product = `2 × (-3) × 5 = -30`
- Remove both negatives (k=1, so only one): best is removing `-3` or `-4`

Consider subarray `[-3, -4, 5]`:
- Remove `-3`: product = `(-4) × 5 = -20`
- Remove `-4`: product = `(-3) × 5 = -15`
- Keep all: product = `(-3) × (-4) × 5 = 60` ✅

Consider subarray `[-3, -4]`:
- Remove `-3`: product = `-4`
- Remove `-4`: product = `-3`
- Keep all: product = `(-3) × (-4) = 12`

Consider subarray `[-4, 5]`:
- Keep all: product = `-20`
- Remove `-4`: product = `5`
- Remove `5`: product = `-4`

The maximum product is **60** from subarray `[-3, -4, 5]` with no removals needed.

**Output:**

```typescript
60
```

---

### **Example 2**

**Input:**

```typescript
nums = [1, -2, -3, 4, -5]
k = 2
```

**Explanation:**

Best strategy: Take subarray `[-2, -3, 4, -5]` and remove `-5` and one other element strategically.

Actually, consider `[1, -2, -3, 4]`:
- Remove `-2, -3`: product = `1 × 4 = 4`

Consider `[-2, -3, 4, -5]`:
- Remove `-5, 4`: product = `(-2) × (-3) = 6`
- Remove `-2, -5`: product = `(-3) × 4 = -12`
- Remove `-3, -5`: product = `(-2) × 4 = -8`
- Keep `-2, -3, 4`: product = `(-2) × (-3) × 4 = 24` ✅

**Output:**

```typescript
24
```

---

### **Example 3**

**Input:**

```typescript
nums = [-2, 0, -1]
k = 0
```

**Explanation:**

With k=0, we cannot remove any elements. Best single element is `0`.

All subarrays:
- `[-2]`: product = `-2`
- `[0]`: product = `0` ✅
- `[-1]`: product = `-1`
- `[-2, 0]`: product = `0`
- `[0, -1]`: product = `0`
- `[-2, 0, -1]`: product = `0`

**Output:**

```typescript
0
```

---

### **Example 4**

**Input:**

```typescript
nums = [2, 3, -2, 4, -1]
k = 1
```

**Explanation:**

Consider subarray `[2, 3, -2, 4]`:
- Remove `-2`: product = `2 × 3 × 4 = 24` ✅

This is the maximum.

**Output:**

```typescript
24
```

---

### **Constraints**

* `1 <= nums.length <= 10^5`
* `-10 <= nums[i] <= 10`
* `0 <= k <= nums.length - 1`
* `nums[i]` can be `0`

---

### **Follow-up**

Can you optimize this to handle the constraints efficiently? Consider:
- How to handle zeros in the array?
- How to maximize product by removing negative numbers strategically?
- What about removing small positive numbers vs. negative numbers?

---

### **Function Signature (TypeScript)**

```typescript
function maxProductWithKRemovals(nums: number[], k: number): number
```

---

### **Starter Code**

```typescript
function maxProductWithKRemovals(nums: number[], k: number): number {
    // Write your code here
    return 0;
}

// Examples
console.log(maxProductWithKRemovals([2, -3, -4, 5], 1)); // Expected output: 60
console.log(maxProductWithKRemovals([1, -2, -3, 4, -5], 2)); // Expected output: 24
console.log(maxProductWithKRemovals([-2, 0, -1], 0)); // Expected output: 0
console.log(maxProductWithKRemovals([2, 3, -2, 4, -1], 1)); // Expected output: 24
```

---

### 💡 **Hints**

1. **Zeros are special**: Any subarray containing 0 can have a product of 0 by including it, or you can split around zeros.

2. **Negative numbers**: An even count of negatives gives a positive product. If you have odd negatives and `k > 0`, consider removing one negative.

3. **Greedy removal**: When removing elements to maximize product:
   - Remove negative numbers that make the product negative
   - Remove the smallest absolute values if all are positive but you need to remove elements
   - Consider removing zeros if they're in the middle of a good subarray

4. **Brute force approach**: Try all possible subarrays, then for each subarray, try all combinations of removing up to k elements.

5. **Optimization**: For each subarray, sort elements by their contribution to the product. Remove elements that hurt the product most.

---

## Explanation — What we are solving

We need to find the maximum product of elements in a contiguous subarray after optionally removing at most `k` elements from it. This combines:
- Subarray enumeration (there are O(n²) subarrays)
- Strategic element removal (up to k elements)
- Product maximization (handling negatives, zeros, and positives)

The key insight: For a given subarray, we want to remove elements that minimize the product or make it negative, while keeping elements that maximize it.

---

## 1) Brute-force approach (beginner friendly)

### Idea:

1. Enumerate all possible contiguous subarrays `[i...j]`.
2. For each subarray, generate all possible combinations of removing up to `k` elements.
3. For each combination, calculate the product of remaining elements.
4. Track the maximum product seen.

This approach has complexity O(n² × C(m,k) × m) where m is subarray length and C(m,k) is combinations. For small inputs, this works but is impractical for large inputs.

### Implementation strategy:
- Use nested loops for subarrays
- Use recursion or bit manipulation to generate removal combinations
- Calculate product for each valid combination

---

## 2) Optimized approach

### Idea:

For each subarray, instead of trying all combinations:

1. **Handle zeros**: If subarray contains zeros, we can always achieve product = 0. But we might do better by splitting around zeros.

2. **Count negatives**: 
   - If negative count is even: product is positive without removals
   - If negative count is odd and k ≥ 1: remove one negative to make product positive

3. **Strategic removal**:
   - Extract all elements from the subarray
   - Sort by "removal priority": 
     - Negatives that make product negative
     - Smallest absolute values
     - Zeros if they don't help
   - Remove top k elements by priority
   - Calculate product of remaining elements

4. **Edge cases**:
   - If we must remove all elements (subarray length ≤ k), skip or handle
   - If only one element remains, that's the product

This is still O(n² × m log m) for sorting elements in each subarray, but much better than full brute force.

---

## Full TypeScript code (both implementations + test harness)

```typescript
// max_product_k_removals.ts
// Run with: npx ts-node max_product_k_removals.ts

type TestCase = {
  id: number;
  name: string;
  nums: number[];
  k: number;
  expected: number;
};

/* ============================
   HELPER FUNCTIONS
   ============================ */

/**
 * Calculate product of an array of numbers
 * Returns 0 for empty array
 */
function productOfArray(arr: number[]): number {
  if (arr.length === 0) return 0;
  let prod = 1;
  for (const num of arr) prod *= num;
  return prod;
}

/**
 * Generate all combinations of removing exactly r elements from array
 * Returns array of arrays (each is the remaining elements after removal)
 */
function* combinationsRemove(arr: number[], r: number): Generator<number[]> {
  const n = arr.length;
  if (r === 0) {
    yield [...arr];
    return;
  }
  if (r >= n) {
    // Can't remove more elements than we have
    return;
  }
  
  // Use bit manipulation to generate combinations of indices to remove
  const totalCombinations = 1 << n; // 2^n
  for (let mask = 0; mask < totalCombinations; mask++) {
    const bitsSet = mask.toString(2).split('0').join('').length;
    if (bitsSet === r) {
      const remaining: number[] = [];
      for (let i = 0; i < n; i++) {
        if ((mask & (1 << i)) === 0) {
          remaining.push(arr[i]);
        }
      }
      yield remaining;
    }
  }
}

/* ============================
   BRUTE FORCE IMPLEMENTATION
   ============================ */

/**
 * Brute force: try all subarrays, all removal combinations, find max product
 * Time: O(n² × 2^m × m) where m is average subarray length - very slow!
 * Space: O(m) for storing subarray elements
 */
function maxProductWithKRemovalsBruteForce(nums: number[], k: number): number {
  const n = nums.length;
  let maxProd = -Infinity;

  // Try all contiguous subarrays
  for (let i = 0; i < n; i++) {
    for (let j = i; j < n; j++) {
      const subarray = nums.slice(i, j + 1);
      const subarrayLen = subarray.length;
      
      // Try removing 0 to min(k, subarrayLen-1) elements
      const maxRemovals = Math.min(k, subarrayLen - 1);
      
      for (let removeCount = 0; removeCount <= maxRemovals; removeCount++) {
        if (removeCount === subarrayLen) continue; // Must keep at least 1 element
        
        if (removeCount === 0) {
          // No removals
          const prod = productOfArray(subarray);
          maxProd = Math.max(maxProd, prod);
        } else {
          // Generate all combinations of removing exactly removeCount elements
          for (const remaining of combinationsRemove(subarray, removeCount)) {
            if (remaining.length > 0) {
              const prod = productOfArray(remaining);
              maxProd = Math.max(maxProd, prod);
            }
          }
        }
      }
    }
  }

  return maxProd;
}

/* ============================
   OPTIMIZED IMPLEMENTATION
   ============================ */

/**
 * Optimized approach: For each subarray, intelligently decide what to remove
 * Time: O(n² × m log m) where m is subarray length
 * Space: O(m)
 */
function maxProductWithKRemovalsOptimized(nums: number[], k: number): number {
  const n = nums.length;
  let maxProd = -Infinity;

  for (let i = 0; i < n; i++) {
    for (let j = i; j < n; j++) {
      const subarray = nums.slice(i, j + 1);
      const subarrayLen = subarray.length;
      
      if (subarrayLen === 0) continue;
      
      // Try different removal counts
      const maxRemovals = Math.min(k, subarrayLen - 1);
      
      for (let removeCount = 0; removeCount <= maxRemovals; removeCount++) {
        if (removeCount >= subarrayLen) continue;
        
        const prod = maxProductAfterRemovals(subarray, removeCount);
        maxProd = Math.max(maxProd, prod);
      }
    }
  }

  return maxProd;
}

/**
 * For a given subarray, find max product after removing exactly removeCount elements
 * Strategy:
 * 1. If removing 0 elements, return product of all
 * 2. Prioritize removing negatives that make product negative
 * 3. Then remove smallest absolute values
 */
function maxProductAfterRemovals(arr: number[], removeCount: number): number {
  if (removeCount === 0) {
    return productOfArray(arr);
  }
  
  if (removeCount >= arr.length) {
    return -Infinity; // Invalid
  }
  
  // Strategy: try removing the "worst" elements
  // Sort by removal priority (elements we want to remove first)
  const indexed = arr.map((val, idx) => ({ val, idx }));
  
  // Priority: 
  // 1. Zeros (if we have better elements)
  // 2. Negatives that would make product negative
  // 3. Elements with smallest absolute value
  
  // Simple heuristic: sort by value, remove smallest (considering signs)
  // This is a greedy approximation
  
  // Better approach: try all combinations smartly
  // For optimization, we'll use a greedy strategy:
  
  // Count negatives
  const negCount = arr.filter(x => x < 0).length;
  const hasZero = arr.includes(0);
  
  // If we have zeros and can remove them, consider that
  if (hasZero && removeCount > 0) {
    const withoutZeros = arr.filter(x => x !== 0);
    if (withoutZeros.length >= arr.length - removeCount) {
      return maxProductAfterRemovals(withoutZeros, Math.max(0, removeCount - (arr.length - withoutZeros.length)));
    }
  }
  
  // If odd negatives and we can remove one, do it
  if (negCount % 2 === 1 && removeCount > 0) {
    // Find the negative with smallest absolute value and remove it
    const negatives = arr.filter(x => x < 0);
    negatives.sort((a, b) => Math.abs(a) - Math.abs(b));
    const toRemove = negatives[0];
    const newArr = [...arr];
    const idx = newArr.indexOf(toRemove);
    newArr.splice(idx, 1);
    return maxProductAfterRemovals(newArr, removeCount - 1);
  }
  
  // Otherwise, remove smallest absolute values
  const sorted = [...arr].sort((a, b) => Math.abs(a) - Math.abs(b));
  const toKeep = sorted.slice(removeCount);
  
  if (toKeep.length === 0) return -Infinity;
  return productOfArray(toKeep);
}

/* ============================
   SELECT MODE
   ============================ */

const MODE: "bruteforce" | "optimized" = "optimized";

/* ============================
   TEST HARNESS
   ============================ */

const tests: TestCase[] = [
  { id: 1, name: "Example 1: Two negatives, k=1", nums: [2, -3, -4, 5], k: 1, expected: 60 },
  { id: 2, name: "Example 2: Multiple negatives, k=2", nums: [1, -2, -3, 4, -5], k: 2, expected: 24 },
  { id: 3, name: "Example 3: With zero, k=0", nums: [-2, 0, -1], k: 0, expected: 0 },
  { id: 4, name: "Example 4: Remove one negative", nums: [2, 3, -2, 4, -1], k: 1, expected: 24 },
  { id: 5, name: "All positive, k=0", nums: [2, 3, 4], k: 0, expected: 24 },
  { id: 6, name: "All positive, k=1", nums: [2, 3, 4], k: 1, expected: 12 },
  { id: 7, name: "Single element", nums: [5], k: 0, expected: 5 },
  { id: 8, name: "Single negative", nums: [-5], k: 0, expected: -5 },
  { id: 9, name: "Two elements, both negative, k=0", nums: [-2, -3], k: 0, expected: 6 },
  { id: 10, name: "Two elements, both negative, k=1", nums: [-2, -3], k: 1, expected: -2 },
  { id: 11, name: "All zeros", nums: [0, 0, 0], k: 0, expected: 0 },
  { id: 12, name: "Mix with zeros, k=1", nums: [2, 0, -3, 4], k: 1, expected: 8 },
  { id: 13, name: "Large negative product", nums: [-1, -2, -3, -4], k: 0, expected: 24 },
  { id: 14, name: "Remove to maximize", nums: [1, 2, -1, 3], k: 1, expected: 6 },
  { id: 15, name: "Strategic removal", nums: [-2, 3, -4], k: 1, expected: 24 },
];

function runTests() {
  const func = MODE === "optimized" ? maxProductWithKRemovalsOptimized : maxProductWithKRemovalsBruteForce;
  console.log(`Running tests in MODE="${MODE}" using function: ${func.name}\n`);

  const results: { 
    id: number; 
    name: string; 
    passed: boolean; 
    nums: number[]; 
    k: number; 
    expected: number; 
    actual: number | string 
  }[] = [];

  for (const tc of tests) {
    let actual: number | string;
    try {
      const out = func(tc.nums, tc.k);
      actual = out;
      const passed = out === tc.expected;
      results.push({ 
        id: tc.id, 
        name: tc.name, 
        passed, 
        nums: tc.nums, 
        k: tc.k, 
        expected: tc.expected, 
        actual: out 
      });
    } catch (err: any) {
      actual = `ERROR: ${err?.message || String(err)}`;
      results.push({ 
        id: tc.id, 
        name: tc.name, 
        passed: false, 
        nums: tc.nums, 
        k: tc.k, 
        expected: tc.expected, 
        actual 
      });
    }
  }

  // Summary
  const passedCount = results.filter(r => r.passed).length;
  const failed = results.filter(r => !r.passed);

  console.log("===========================================");
  console.log(`Maximum Subarray Product with K Removals — Test Run`);
  console.log(`Total tests: ${tests.length}`);
  console.log(`Passed: ${passedCount}`);
  console.log(`Failed: ${failed.length}`);
  console.log("===========================================\n");

  for (const r of results) {
    const mark = r.passed ? "✅ PASS" : "❌ FAIL";
    console.log(`${mark} [#${r.id}] ${r.name}`);
    if (!r.passed) {
      console.log(`   Input: nums=${JSON.stringify(r.nums)}, k=${r.k}`);
      console.log(`   Expected: ${r.expected}`);
      console.log(`   Actual: ${r.actual}`);
      console.log("");
    }
  }

  if (failed.length === 0) {
    console.log("🎉 All test cases passed!");
  } else {
    console.log(`\n⚠️  ${failed.length} test(s) failed. Review the cases above.`);
  }
}

runTests();
```

---

## Complexity Analysis

### Brute Force:
- **Time**: O(n² × 2^m × m) where m is average subarray length
  - O(n²) subarrays
  - For each subarray of length m, we try removing 0 to k elements
  - Each removal count has C(m, r) combinations ≈ 2^m in worst case
  - Each combination takes O(m) to compute product
- **Space**: O(m) for storing subarray and combinations

### Optimized:
- **Time**: O(n² × m × k) with greedy removal strategy
  - O(n²) subarrays
  - For each subarray, try k+1 removal counts
  - Each removal strategy takes O(m) with greedy approach
- **Space**: O(m)

---

## Key Insights

1. **Product properties**:
   - Even number of negatives → positive product
   - Odd number of negatives → negative product (remove one negative if possible)
   - Zero makes product zero (can be good or bad)

2. **Removal strategy**:
   - Remove negatives that keep product negative
   - Remove smallest absolute values if all same sign
   - Consider splitting around zeros

3. **This problem is NP-hard** in general (subset selection for max product), but with small k and greedy heuristics, we can get good solutions.

---

## Notes

This problem is significantly harder than "Balanced Segment Split" because:
- It involves product instead of sum (more complex behavior with negatives/zeros)
- The removal aspect adds combinatorial complexity
- Multiple competing strategies (remove negatives vs. small values vs. zeros)
- Requires careful handling of edge cases

The optimized solution uses greedy heuristics that work well in practice but may not always find the absolute maximum for complex cases. A fully optimal solution would require dynamic programming or exhaustive search with pruning.
