# Two Sum

Problem Number: 1

Difficulty: Easy

Language: 1class Solution {
2    public int[] twoSum(int[] nums, int target) {
3        for(int i=0;i<nums.length;i++){
4            for(int j=i+1;j<nums.length;j++){
5                if(nums[i]+nums[j]==target){
6                    return new int[]{i,j};
7                }
8            }
9        }
10        return new int[]{};
11     }
12    
13}

Problem URL:
https://leetcode.com/problems/two-sum/

Submission Date:
2026-11-17 04:33:46

Generated automatically by LeetSync.
