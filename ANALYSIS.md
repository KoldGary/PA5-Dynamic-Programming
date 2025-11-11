# CS 366 - PA5: Dynamic Programming Analysis

**Name:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Date:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

---

## Part 2: Written Analysis

### 1. Manual Trace

Trace the following instance of the `dynamicKnapsack` algorithm by filling in the `exist` and `belong` grids:

- **n = 4** (number of items)
- **k = 10** (knapsack capacity)
- **S = [2, 3, 5, 6]** (item sizes, using 1-indexed notation: S[1]=2, S[2]=3, S[3]=5, S[4]=6)

#### exist grid (mark T for true, F for false)

```
exist | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
------|---|---|---|---|---|---|---|---|---|---|----|
  0   |   |   |   |   |   |   |   |   |   |   |    |
  1   |   |   |   |   |   |   |   |   |   |   |    |
  2   |   |   |   |   |   |   |   |   |   |   |    |
  3   |   |   |   |   |   |   |   |   |   |   |    |
  4   |   |   |   |   |   |   |   |   |   |   |    |
```

#### belong grid (mark T for true, F for false)

```
belong| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
------|---|---|---|---|---|---|---|---|---|---|----|
  0   |   |   |   |   |   |   |   |   |   |   |    |
  1   |   |   |   |   |   |   |   |   |   |   |    |
  2   |   |   |   |   |   |   |   |   |   |   |    |
  3   |   |   |   |   |   |   |   |   |   |   |    |
  4   |   |   |   |   |   |   |   |   |   |   |    |
```

#### Traceback Process

**Instructions:** Show the traceback path through your completed grids by **bolding** or *italicizing* the positions you visit as you trace back from the solution.

**Final Solution:**

- Items in knapsack (by index): \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
- Total size achieved: \_\_\_\_\_\_\_\_\_\_
- Wasted space: \_\_\_\_\_\_\_\_\_\_

---

### 2. Complexity Analysis

#### Time Complexity

**Time complexity in Θ-notation:**

Θ(\_\_\_\_\_\_\_\_\_\_\_\_)

**Explanation** (analyze the nested loops in the algorithm):

[Your explanation here]

#### Space Complexity

**Space complexity in Θ-notation:**

Θ(\_\_\_\_\_\_\_\_\_\_\_\_)

**Explanation:**

[Your explanation here]

---

### 3. Algorithm Limitations

#### Question 1: When does this approach become impractical?

For what values of n and k would this dynamic programming approach become impractical?

**Answer:**

[Your answer here]

#### Question 2: Pseudo-polynomial time

Why is this algorithm considered "pseudo-polynomial" time?

**Answer:**

[Your answer here]

---

## Reflection (Optional)

Any additional observations, challenges, or insights from this assignment:

[Your reflection here]
