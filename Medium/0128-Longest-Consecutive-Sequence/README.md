# Longest Consecutive Sequence

Problem Number: 128

Difficulty: Medium

Language: 1
2import java.util.*;
3
4class Solution {
5    public int longestConsecutive(int[] nums) {
6        if (nums.length == 0) {
7            return 0;
8        }
9
10        Arrays.sort(nums);
11
12        int count = 1;
13        int max = 1;
14
15        for (int i = 1; i < nums.length; i++) {
16            if (nums[i] == nums[i - 1]) {
17                continue;
18            }
19
20            if (nums[i] == nums[i - 1] + 1) {
21                count++;
22            } else {
23                count = 1;
24            }
25
26            max = Math.max(max, count);
27        }
28
29        return max;
30    }
31}
32

Problem URL:
https://leetcode.com/problems/longest-consecutive-sequence/

Submission Date:
2026-10-14 02:50:09

Generated automatically by LeetSync.
