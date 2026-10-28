# Leetcode_Day88
# Day 88 – Maximum Depth of Binary Tree

**LeetCode Problem:** [104. Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)  
**Difficulty:** Easy  
**Language:** Java  
**Topic:** Binary Tree, Recursion, Depth-First Search (DFS)

## Problem Statement

Given the root of a binary tree, return its maximum depth.

The maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.

## Approach: Recursion

I solved this problem using recursion.

1. If the current node is `null`, return `0` because an empty tree has no depth.
2. Recursively calculate the maximum depth of the left subtree.
3. Recursively calculate the maximum depth of the right subtree.
4. Take the larger depth and add `1` for the current node.
5. Return the result.

### Java Solution

```java
class Solution {
    public int maxDepth(TreeNode root) {
        if (root == null) return 0;

        int left = maxDepth(root.left);
        int right = maxDepth(root.right);

        return 1 + Math.max(left, right);
    }
}
```

## Complexity Analysis

- **Time Complexity:** `O(n)` — Every node is visited once.
- **Space Complexity:** `O(h)` — The recursive call stack depends on the height of the tree. In the worst case, it can be `O(n)`.

Here, `n` is the number of nodes and `h` is the height of the tree.

## What I Learned

- How recursion works with binary trees.
- How to calculate the depth of a tree using its left and right subtrees.
- How `Math.max()` helps choose the deeper subtree.
- Why a clear base case is essential in recursive solutions.

## Takeaway

This problem reminded me that a bigger problem can become easier when we break it into smaller problems and solve each one step by step.

**Day 88 complete — one more step toward becoming a better problem solver!** 🌱
