# Product of Array Except Self

Problem Number: 238

Difficulty: Medium

Language: 1class Solution {
2    public int[] productExceptSelf(int[] nums) {
3        int n=nums.length;
4        int prefix[]=new int[nums.length];
5        int suffix[]=new int[nums.length];
6        int answer[]=new int[nums.length];
7
8        prefix[0]=1;
9        for(int i=1;i<n;i++){
10            prefix[i]=prefix[i-1]*nums[i-1];
11        }
12
13        suffix[n-1]=1;
14        for(int i=n-2;i>=0;i--){
15            suffix[i]=suffix[i+1]*nums[i+1];
16        }
17
18        for(int i=0;i<n;i++){
19            answer[i]=prefix[i]*suffix[i];
20        }
21        return answer;
22    }
23}

Problem URL:
https://leetcode.com/problems/product-of-array-except-self/

Submission Date:
2026-09-01 14:29:11

Generated automatically by LeetSync.
