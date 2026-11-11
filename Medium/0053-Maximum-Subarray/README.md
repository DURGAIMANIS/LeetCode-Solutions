# Maximum Subarray

Problem Number: 53

Difficulty: Medium

Language: 1class Solution {
2    public int maxSubArray(int[] nums) {
3        int currsum=0;
4        int maxsum=nums[0];
5        // Time Complexity: O(n)
6        // Space Complexity: O(1)
7
8        //i need to find maxsum 
9        for(int i=0;i<nums.length;i++){
10            //add every element one by one
11            currsum+=nums[i];
12            //find maximum sum at every element come to add
13            maxsum=Math.max(maxsum,currsum);
14            //but if the negetive comes, then  make it zero
15            if(currsum<0){
16                currsum=0;
17            }    
18        }
19        return maxsum;
20
21        //Keep adding elements. If the current sum becomes worse than starting fresh, start a new subarray.
22        
23
24    }
25}

Problem URL:
https://leetcode.com/problems/maximum-subarray/

Submission Date:
2026-11-11 01:51:31

Generated automatically by LeetSync.
