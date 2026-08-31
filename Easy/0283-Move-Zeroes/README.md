# Move Zeroes

Problem Number: 283

Difficulty: Easy

Language: 1class Solution {
2    public void moveZeroes(int[] nums) {
3        int left=0;
4        int right=0;
5        while(right<nums.length){
6            if(nums[right]!=0){
7                int temp=nums[right];
8                nums[right]=nums[left];
9                nums[left]=temp;
10                left++;
11            }
12            right++;
13        }
14    }
15}

Problem URL:
https://leetcode.com/problems/move-zeroes/

Submission Date:
2026-08-31 14:35:17

Generated automatically by LeetSync.
