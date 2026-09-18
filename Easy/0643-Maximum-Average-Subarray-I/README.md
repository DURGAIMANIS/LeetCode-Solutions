# Maximum Average Subarray I

Problem Number: 643

Difficulty: Easy

Language: 1class Solution {
2    public double findMaxAverage(int[] nums,int k) {
3        double sum=0;
4        for(int i=0;i<k;i++){
5            sum+=nums[i];
6        }
7        double max=sum;
8        for(int i=k;i<nums.length;i++){
9            sum+=nums[i];
10            sum-=nums[i-k];
11            max=Math.max(max,sum);
12        }
13        return max/k;
14    }
15}

Problem URL:
https://leetcode.com/problems/maximum-average-subarray-i/

Submission Date:
2026-09-18 11:46:15

Generated automatically by LeetSync.
