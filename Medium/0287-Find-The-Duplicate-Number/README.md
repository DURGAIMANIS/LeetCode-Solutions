# Find the Duplicate Number

Problem Number: 287

Difficulty: Medium

Language: 1class Solution {
2    public int findDuplicate(int[] nums) {
3
4        Arrays.sort(nums);
5
6        for (int i = 1; i < nums.length; i++) {
7
8            if (nums[i] == nums[i - 1]) {
9                return nums[i];
10            }
11        }
12
13        return -1;
14    }
15}

Problem URL:
https://leetcode.com/problems/find-the-duplicate-number/

Submission Date:
2026-09-01 15:10:54

Generated automatically by LeetSync.
