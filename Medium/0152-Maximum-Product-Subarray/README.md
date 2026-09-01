# Maximum Product Subarray

Problem Number: 152

Difficulty: Medium

Language: 1class Solution {
2    public int maxProduct(int[] nums) {
3        int max=nums[0];
4        int min=nums[0];
5        int answer=nums[0];
6        for(int i=1;i<nums.length;i++){
7            if(nums[i]<0){
8                int temp=max;
9                max=min;
10                min=temp;
11            }
12
13            max=Math.max(nums[i],max*nums[i]);
14            min=Math.min(nums[i],min*nums[i]);
15            answer=Math.max(answer,max);
16        }
17        return answer;
18
19    }
20}
21

Problem URL:
https://leetcode.com/problems/maximum-product-subarray/

Submission Date:
2026-09-01 03:25:56

Generated automatically by LeetSync.
