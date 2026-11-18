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
10            }else if(nums[i]<target){
11                index=i;
12            }else if(nums[i]>target){
13                return i;
14            }
15        }
16        return nums.length;
17    }
18}

Problem URL:
https://leetcode.com/problems/search-insert-position/

Submission Date:
2026-11-18 10:26:09

Generated automatically by LeetSync.
