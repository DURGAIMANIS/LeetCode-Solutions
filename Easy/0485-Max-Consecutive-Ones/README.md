# Max Consecutive Ones

Problem Number: 485

Difficulty: Easy

Language: 1class Solution {
2    public int findMaxConsecutiveOnes(int[] nums) {
3        int maxcount=0;
4
5        int left=0;
6        int right=nums.length;
7
8        int count=0;
9
10        while(left<right){
11            if(nums[left]==1){
12                count++;
13                maxcount=Math.max(maxcount,count);
14                left++;
15            }else{
16                count=0;
17                left++;
18            }
19        }
20        return maxcount;
21    }
22}

Problem URL:
https://leetcode.com/problems/max-consecutive-ones/

Submission Date:
2026-08-23 12:15:49

Generated automatically by LeetSync.
