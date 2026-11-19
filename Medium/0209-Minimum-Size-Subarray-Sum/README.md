# Minimum Size Subarray Sum

Problem Number: 209

Difficulty: Medium

Language: 1class Solution {
2    public int minSubArrayLen(int target, int[] nums) {
3
4        int left = 0;
5        int sum = 0;
6        int min = Integer.MAX_VALUE;
7
8        for (int right = 0; right < nums.length; right++) {
9
10            sum = sum + nums[right];
11
12            while (sum >= target) {
13
14                int length = right - left + 1;
15
16                if (length < min) {
17                    min = length;
18                }
19
20                sum = sum - nums[left];
21                left++;
22            }
23        }
24
25        if (min == Integer.MAX_VALUE) {
26            return 0;
27        }
28
29        return min;
30    }
31}

Problem URL:
https://leetcode.com/problems/minimum-size-subarray-sum/

Submission Date:
2026-11-19 13:02:26

Generated automatically by LeetSync.
