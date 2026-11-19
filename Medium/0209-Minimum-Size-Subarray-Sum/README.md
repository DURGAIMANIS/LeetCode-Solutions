# Minimum Size Subarray Sum

Problem Number: 209

Difficulty: Medium

Language: 1class Solution {
2    public int minSubArrayLen(int target, int[] nums) {
3        int left = 0;
4        int sum = 0;
5        int min = Integer.MAX_VALUE;
6
7        for (int right = 0; right < nums.length; right++) {
8            sum = sum + nums[right];
9            while (sum >= target) {
10                int length = right - left + 1;
11                if (length < min) {
12                    min = length;
13                }
14                sum = sum - nums[left];
15                left++;
16            }
17        }
18        if (min == Integer.MAX_VALUE) {
19            return 0;
20        }
21        return min;
22    }
23}

Problem URL:
https://leetcode.com/problems/minimum-size-subarray-sum/

Submission Date:
2026-11-19 14:20:32

Generated automatically by LeetSync.
