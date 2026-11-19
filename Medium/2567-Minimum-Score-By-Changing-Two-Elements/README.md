# Minimum Score by Changing Two Elements

Problem Number: 2567

Difficulty: Medium

Language: 1class Solution {
2    public int minimizeSum(int[] nums) {
3        int n=nums.length;
4        if(nums.length<=3){
5            return 0;
6        }
7
8        Arrays.sort(nums);
9        int a=nums[n-1]-nums[2];
10        int b=nums[n-3]-nums[0];
11        int c=nums[n-2]-nums[1];
12
13        int min=Math.min(a,Math.min(b,c));
14        return min;
15    }
16}

Problem URL:
https://leetcode.com/problems/minimum-score-by-changing-two-elements/

Submission Date:
2026-11-19 03:59:53

Generated automatically by LeetSync.
