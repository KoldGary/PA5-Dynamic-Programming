# CS 366 - PA5: Dynamic Programming Analysis

**Name:** Adrian Gary
**Date:** 11/30/25
---

## Part 2: Written Analysis

### 1. Manual Trace

Trace the following instance of the `dynamicKnapsack` algorithm by filling in the `exist` and `belong` grids:

- **n = 4** (number of items)
- **k = 10** (knapsack capacity)
- **S = [2, 3, 5, 6]** (item sizes, using 1-indexed notation: S[1]=2, S[2]=3, S[3]=5, S[4]=6)

#### exist grid (mark T for true, F for false)

```
exist |  0 |  1 |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 | 10 |
------|----|----|----|----|----|----|----|----|----|----|----|
  0   |  T |  F |  F |  F |  F |  F |  F |  F |  F |  F |  F |
  1   |  T |  F | **T** |  F |  F |  F |  F |  F |  F |  F |  F |
  2   |  T |  F |  T |  T |  F | **T** |  F |  F |  F |  F |  F |
  3   |  T |  F |  T |  T |  F |  T |  F |  T |  T |  F | **T** |
  4   |  T |  F |  T |  T |  F |  T |  T |  T |  T |  T | **T** |
```

#### belong grid (mark T for true, F for false)

```
belong|  0 |  1 |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 | 10 |
------|----|----|----|----|----|----|----|----|----|----|----|
  0   |  F |  F |  F |  F |  F |  F |  F |  F |  F |  F |  F |
  1   |  F |  F | **T** |  F |  F |  F |  F |  F |  F |  F |  F |
  2   |  F |  F |  F |  F |  F | **T** |  F |  F |  F |  F |  F |
  3   |  F |  F |  F |  F |  F |  T |  F |  T |  T |  F | **T** |
  4   |  F |  F |  F |  F |  F |  F |  T |  F |  T |  T | **F** |
```

#### Traceback Process

**Instructions:** Show the traceback path through your completed grids by **bolding** or *italicizing* the positions you visit as you trace back from the solution.

**Final Solution:**

- Items in knapsack (by index): 0, 1, 2(sizes: 2, 3, 5)
- Total size achieved: 2+3+5=10
- Wasted space: k - total = 10 - 10 = 0

---

### 2. Complexity Analysis

#### Time Complexity

**Time complexity in Θ-notation:**

Θ(nk)

**Explanation** (analyze the nested loops in the algorithm):

The DP fills an (n+1) × (k+1) table, since each cell only constant-time work.
So the total work = number of cells = n × k.

#### Space Complexity

**Space complexity in Θ-notation:**

Θ(nk)

**Explanation:**

store the two DP tables (exist and belong), each of size (n+1) × (k+1), so total memory grows to the proportional to n × k

---

### 3. Algorithm Limitations

#### Question 1: When does this approach become impractical?

For what values of n and k would this dynamic programming approach become impractical?

**Answer:**

When k is very large the Memory and time both blow up, because the DP tables require n × k space and time.

#### Question 2: Pseudo-polynomial time

Why is this algorithm considered "pseudo-polynomial" time?

**Answer:**

the running time depends on the numeric value of k, not the number of bits needed to represent k,
So it is polynomial in k, and is polynomial is not the true input size (log k).

---

## Reflection (Optional)

Any additional observations, challenges, or insights from this assignment:

[Your reflection here]
