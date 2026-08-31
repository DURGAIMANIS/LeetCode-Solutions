# Move Zeroes

Problem Number: 283

Difficulty: Easy

Language: 1class Solution {
2    public void moveZeroes(int[] nums) {
3        int left=0;
4        for(int right=0;right<nums.length;right++){
5            if(nums[right]!=0){
6                int temp=nums[left];
7                nums[left]=nums[right];
8                nums[right]=temp;
9                left++;
10            }
11        }
12    }
13}

Problem URL:
https://leetcode.com/problems/move-zeroes/

Submission Date:
2026-08-31 14:28:42

Generated automatically by LeetSync.
