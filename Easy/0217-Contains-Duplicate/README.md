# Contains Duplicate

Problem Number: 217

Difficulty: Easy

Language: 1class Solution {
2    public boolean containsDuplicate(int[] nums) {
3        HashSet<Integer> set=new HashSet<>();
4        for(int i=0;i<nums.length;i++){
5            if(set.contains(nums[i])){
6                return true;
7            }else{
8                set.add(nums[i]);
9            }
10        }
11        return false;
12    }
13}

Problem URL:
https://leetcode.com/problems/contains-duplicate/

Submission Date:
2026-08-31 16:13:24

Generated automatically by LeetSync.
