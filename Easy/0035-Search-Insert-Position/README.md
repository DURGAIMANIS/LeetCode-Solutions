# Search Insert Position

Problem Number: 35

Difficulty: Easy

Language: 1class Solution {
2    public int searchInsert(int[] nums, int target) {
3        int left=0;
4        int right=nums.length-1;
5        int index=-1;
6
7        for(int i=0;i<nums.length;i++){
8            if(nums[i]==target){
9                return i;
10            }else if(nums[i]>target){
11                return i;
12            }
13        }
14        return nums.length;
15    }
16}

Problem URL:
https://leetcode.com/problems/search-insert-position/

Submission Date:
2026-11-18 10:28:17

Generated automatically by LeetSync.
