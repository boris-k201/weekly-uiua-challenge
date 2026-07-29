# 2026-07-22

## Task 1: Diff-K

You are given an array @N of positive integers (sorted) and another non negative integer k.
Write a script to find if there exists 2 indices i and j such that A[i] - A[j] = k and i != j.
It should print the pairs of indices, if any such pairs exist.
Example:
@N = (2, 7, 9) $k = 2
Output : 2,1

### Uiua

```
6
[70 49 22 48 9 86 81 87 58 54 93 28]
⊸⧅≠2
⊸(≡₁/-)
⊃(⊚=⊙(◌◌)|∘◌|∘◌◌◌)
⊏
≡₁(&p$"_ - _ = _"°⊟⇌⊙⊢)
```

## Task 2: Path Sum

You are given a binary tree and a sum, write a script to find if the tree has a path such that adding up all the values along the path equals the given sum. Only complete paths (from root to leaf node) may be considered for a sum.

Example:
Given the below binary tree and sum = 22,

     5
    / \
   4   8
  /   / \
11   13  9

/ \
7 2 1

For the given binary tree, the partial path sum 5 → 8 → 9 = 22 is not valid.
The script should return the path 5 → 4 → 11 → 2 whose sum is 22.
