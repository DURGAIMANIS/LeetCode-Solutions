# Search in Rotated Sorted Array

Problem Number: 33

Difficulty: Medium

Language: 1class Solution {
2    public int search(int[] nums, int target) {
3        //we can use linear search
4        for (int i=0;i<nums.length; i++) {
5            if (nums[i]==target){
6                return i;
7            }
8        }
9        return -1;
10    }
11}

Problem URL:
https://leetcode.com/problems/search-in-rotated-sorted-array/

Submission Date:
2026-11-19 06:24:04

Generated automatically by LeetSync.
