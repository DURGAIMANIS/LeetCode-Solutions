# Remove Duplicates from Sorted Array

Problem Number: 26

Difficulty: Easy

Language: 1class Solution {
2    public int removeDuplicates(int[] nums) {
3        int k=1;
4       
5        for(int i=1;i<nums.length;i++){
6            if(nums[i]!=nums[i-1]){
7                nums[k]=nums[i];
8                k++;
9            }
10        }
11        return k;
12    }
13}

Problem URL:
https://leetcode.com/problems/remove-duplicates-from-sorted-array/

Submission Date:
2026-09-14 05:07:10

Generated automatically by LeetSync.
