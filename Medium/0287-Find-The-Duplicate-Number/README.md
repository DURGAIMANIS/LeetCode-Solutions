# Find the Duplicate Number

Problem Number: 287

Difficulty: Medium

Language: 1class Solution {
2    public int findDuplicate(int[] nums) {
3        HashSet<Integer> set=new HashSet<>();
4        for(int i=0;i<nums.length;i++){
5            if(set.contains(nums[i])){
6                return nums[i];
7            }
8            set.add(nums[i]);
9        }
10        return 0;
11    }
12}

Problem URL:
https://leetcode.com/problems/find-the-duplicate-number/

Submission Date:
2026-09-01 14:31:56

Generated automatically by LeetSync.
