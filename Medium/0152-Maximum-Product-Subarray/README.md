# Maximum Product Subarray

Problem Number: 152

Difficulty: Medium

Language: 1class Solution {
2    public int maxProduct(int[] nums) {
3        int max=nums[0];
4        int min=nums[0];
5        int answer=nums[0];
6        // Time Complexity: O(n)
7        // Space Complexity: O(1)
8        for(int i=1;i<nums.length;i++){
9            if(nums[i]<0){
10                int temp=max;
11                max=min;
12                min=temp;
13            }
14
15            max=Math.max(nums[i],max*nums[i]);//stores max
16            min=Math.min(nums[i],min*nums[i]);//stores min
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
2026-11-11 01:58:46

Generated automatically by LeetSync.
