# Find the Duplicate Number

Problem Number: 287

Difficulty: Medium

Language: 1class Solution {
2    public int findDuplicate(int[] nums) {
3        boolean arr[]=new boolean[nums.length];
4        for(int i=0;i<nums.length;i++){
5            if(arr[nums[i]]==true){
6                return nums[i];
7            }else{
8                arr[nums[i]]=true;
9            }
10        }
11        return -1;
12    }
13}

Problem URL:
https://leetcode.com/problems/find-the-duplicate-number/

Submission Date:
2026-09-06 12:49:02

Generated automatically by LeetSync.
