# Product of Array Except Self

Problem Number: 238

Difficulty: Medium

Language: 1class Solution {
2    public int[] productExceptSelf(int[] nums) {
3       int[] arr = new int[nums.length];
4
5        // Product of all elements to the left
6        int before = 1;
7
8        for (int i = 0; i < nums.length; i++) {
9            arr[i] = before;
10            before *= nums[i];
11        }
12
13        // Product of all elements to the right
14        int after = 1;
15
16        for (int i = nums.length - 1; i >= 0; i--) {
17            arr[i] *= after;
18            after *= nums[i];
19        }
20
21        return arr;
22        
23    }
24}

Problem URL:
https://leetcode.com/problems/product-of-array-except-self/

Submission Date:
2026-08-10 11:56:14

Generated automatically by LeetSync.
