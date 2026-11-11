# Move Zeroes

Problem Number: 283

Difficulty: Easy

Language: 1class Solution {
2    public void moveZeroes(int[] nums) {
3        int left=0;
4        int right=0;
5        // Time Complexity: O(n)
6        // Space Complexity: O(1)
7        while(right<=nums.length-1){
8            if(nums[right]!=0){
9                int temp=nums[left];
10                nums[left]=nums[right];
11                nums[right]=temp;
12                left++;
13            }
14            right++;
15        }
16    }
17}

Problem URL:
https://leetcode.com/problems/move-zeroes/

Submission Date:
2026-11-11 01:39:13

Generated automatically by LeetSync.
