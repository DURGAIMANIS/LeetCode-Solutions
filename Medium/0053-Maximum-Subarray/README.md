# Maximum Subarray

Problem Number: 53

Difficulty: Medium

Language: 1class Solution {
2    public int maxSubArray(int[] nums) {
3        int currsum=0;
4        int maxsum=nums[0];
5
6        //i need to find maxsum 
7        for(int i=0;i<nums.length;i++){
8            //add every element one by one
9            currsum+=nums[i];
10            //find maximum sum at every element come to add
11            maxsum=Math.max(maxsum,currsum);
12            //but if the negetive comes, then  make it zero
13            if(currsum<0){
14                currsum=0;
15            }    
16        }
17        return maxsum;
18
19        //Keep adding elements. If the current sum becomes worse than starting fresh, start a new subarray.
20        
21
22    }
23}

Problem URL:
https://leetcode.com/problems/maximum-subarray/

Submission Date:
2026-09-01 02:49:47

Generated automatically by LeetSync.
