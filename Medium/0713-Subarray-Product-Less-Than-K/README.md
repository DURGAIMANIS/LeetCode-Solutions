# Subarray Product Less Than K

Problem Number: 713

Difficulty: Medium

Language: 1class Solution {
2    public int numSubarrayProductLessThanK(int[] nums, int k) {
3        if(k<=1) return 0;
4        int product=1;
5        int left=0;
6        int count=0;
7
8        for(int right=0;right<nums.length;right++){
9            product*=nums[right];
10            
11            while(product>=k){
12                product/=nums[left];
13                left++;
14            }
15            count+=right-left+1;
16        }
17        return count;
18    }
19}

Problem URL:
https://leetcode.com/problems/subarray-product-less-than-k/

Submission Date:
2026-08-23 13:12:17

Generated automatically by LeetSync.
