# Balanced Binary Tree

Problem Number: 110

Difficulty: Easy

Language: 1/**
2 * Definition for a binary tree node.
3 * public class TreeNode {
4 *     int val;
5 *     TreeNode left;
6 *     TreeNode right;
7 *     TreeNode() {}
8 *     TreeNode(int val) { this.val = val; }
9 *     TreeNode(int val, TreeNode left, TreeNode right) {
10 *         this.val = val;
11 *         this.left = left;
12 *         this.right = right;
13 *     }
14 * }
15 */
16class Solution {
17    public boolean isBalanced(TreeNode root) {
18
19        if (root == null) return true;
20
21        int left = maxDepth(root.left);
22        int right = maxDepth(root.right);
23
24        if (Math.abs(left - right) > 1) {
25            return false;
26        }
27
28        return isBalanced(root.left) && isBalanced(root.right);
29    }
30
31    public int maxDepth(TreeNode root) {
32        if (root == null) return 0;
33
34        int left = maxDepth(root.left);
35        int right = maxDepth(root.right);
36
37        return 1 + Math.max(left, right);
38    }
39}

Problem URL:
https://leetcode.com/problems/balanced-binary-tree/

Submission Date:
2026-10-30 05:16:44

Generated automatically by LeetSync.
