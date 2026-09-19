# Range Sum Query - Immutable

Problem Number: 303

Difficulty: Easy

Language: nums = [-2, 0, 3, -5, 2, -1]
ps = [-2,-2,1,-4,-2,-3] // prefix sum

[0,2] = ps[2] + (nums[0] - ps[0]) = 1 + (-2 - (-2)) = 1
[2,5] = ps[5] + (nums[2] - ps[2]) = -3 + (3 - 1) = -1
[0,5] = ps[5] + (nums[0] - ps[0]) =  -3 + (-2 - (-2)) = -3
[2,4] = ps[4] + (nums[2] - ps[2]) =  -2 + (3-1) = 0

Problem URL:
https://leetcode.com/problems/range-sum-query-immutable/

Submission Date:
2026-09-19 03:41:55

Generated automatically by LeetSync.
