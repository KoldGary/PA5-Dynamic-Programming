# PA5 Quick Start Guide

## Building and Running Your Code

This project uses Gradle for building and running Java code. You don't need to install Gradle - the `gradlew` script will download it automatically.

### Build the Project

```bash
./gradlew build
```

### Run Your Program

```bash
./gradlew run --args="items1.txt"
```

Then enter `n` and `k` when prompted (for items1.txt, use n=5 and k=16).

### Clean Build Artifacts

```bash
./gradlew clean
```

### Run Tests (when you add them)

```bash
./gradlew test
```

## Project Structure

```
pa5/
├── src/
│   └── main/
│       └── java/
│           └── edu/
│               └── wne/
│                   └── cs366/
│                       └── Knapsack.java    ← Your code here
├── items1.txt                               ← Test input files
├── items2.txt
├── items3.txt
├── build.gradle                             ← Gradle configuration
└── README.md                                ← Full assignment description
```

## Your Tasks

1. **Implement `dynamicKnapsack()` method**

   - Fill in the DP algorithm following the pseudocode from class
   - Use the `exist` and `belong` arrays

2. **Implement `findSolution()` method**

   - Trace back through the DP tables to find selected items
   - Return a list of item indices

3. **Test your implementation**

   - Run with all three test files
   - Verify your total sizes match the expected outputs

4. **Write analysis.pdf**
   - Answer the complexity analysis questions
   - Explain time/space trade-offs

## Test Cases

### Test 1: items1.txt

```bash
echo -e "5\n16" | ./gradlew run --args="items1.txt" --quiet
```

Expected: Total size = 16

### Test 2: items2.txt

```bash
echo -e "4\n13" | ./gradlew run --args="items2.txt" --quiet
```

Expected: Total size = 12 or 13

### Test 3: items3.txt

```bash
echo -e "12\n35" | ./gradlew run --args="items3.txt" --quiet
```

Expected: Total size = 34 or 35

## Debugging Tips

1. **Print the DP tables:**
   Uncomment this line in `main()`:

   ```java
   knapsack.printTables();
   ```

2. **Trace by hand first:**
   Use a small example (n=3, k=10) and trace the algorithm step by step on paper before coding.

3. **Check base cases:**
   Make sure `exist[0][0] = true` and all other `exist[0][j] = false`

4. **Watch for array indices:**
   The pseudocode uses 1-indexed arrays, but Java uses 0-indexed arrays. The starter code uses arrays of size `[n+1][k+1]` to make this easier.
