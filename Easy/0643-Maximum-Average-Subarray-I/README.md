# Maximum Average Subarray I

Problem Number: 643

Difficulty: Easy

Language: 1class Solution {
2    public double findMaxAverage(int[] nums,int k) {
3        double sum=0;
4        double maxval=Double.NEGATIVE_INFINITY;
5        for(int i=0;i<k;i++){
6            sum+=nums[i];
7        }
8        maxval=sum/k;
9        for(int i=k;i<nums.length;i++){
10            sum-=nums[i-k];
11            sum+=nums[i];
12            double avg=sum/k;
13            maxval=Math.max(maxval,avg);
14        }
15        return maxval;
16    }
17}

Problem URL:
https://leetcode.com/problems/maximum-average-subarray-i/

Submission Date:
2026-08-05 16:30:11

Generated automatically by LeetSync.
