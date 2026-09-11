# LeetCode 172 - Factorial Trailing Zeroes

## Problem

Given an integer `n`, return the number of trailing zeroes in `n!`.

A trailing zero is created whenever a number contains a factor of `10`.

Since:

```text
10 = 2 × 5
```

we need to count the number of pairs of `2` and `5`.

There are usually more factors of `2` than `5`, so the answer depends on the number of factors of `5`.

## Approach

Instead of calculating the complete factorial, count how many times `5` appears as a factor.

We repeatedly divide `n` by `5`:

```text
n // 5
n // 25
n // 125
...
```

The additional divisions count numbers containing multiple factors of `5`.

### Example

For:

```text
n = 25
```

```text
25 // 5 = 5
25 // 25 = 1
```

Total:

```text
5 + 1 = 6
```

Therefore:

```text
25! has 6 trailing zeroes
```

## Algorithm

1. Initialize `count = 0`.
2. Divide `n` by `5`.
3. Add the result to `count`.
4. Continue while `n > 0`.
5. Return `count`.

## Complexity

* **Time Complexity:** `O(log₅ n)`
* **Space Complexity:** `O(1)`

## Key Concepts

* Factorials
* Factors of 5
* Integer division
* Mathematical counting
* Efficient algorithms

## What I Learned

This problem shows why we should not always calculate the complete factorial.

For large values of `n`, calculating `n!` would be inefficient. Instead, we can use mathematics and count the factors of `5` directly.

## LeetCode Details

* **Problem:** 172
* **Title:** Factorial Trailing Zeroes
* **Language:** Python
* **Difficulty:** Medium

## Author

T.Nandhini
