# Maximum Product Subarray

Problem Number: 152

Difficulty: Medium

Language: 1class Solution {
2    public int maxProduct(int[] nums) {
3        int max=nums[0];
4        int min=nums[0];
5        int answer=nums[0];
6
7        for(int i=1;i<nums.length;i++){
8            if(nums[i]<0){
9                int temp=max;
10                max=min;
11                min=temp;
12            }
13
14            max=Math.max(nums[i],max*nums[i]);
15            min=Math.min(nums[i],min*nums[i]);
16
17            answer=Math.max(answer,max);
18        }
19        return answer;
20
21    }
22}
23

Problem URL:
https://leetcode.com/problems/maximum-product-subarray/

Submission Date:
2026-09-01 03:13:16

Generated automatically by LeetSync.
