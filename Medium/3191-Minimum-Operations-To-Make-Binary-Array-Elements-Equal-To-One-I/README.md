# Minimum Operations to Make Binary Array Elements Equal to One I

Problem Number: 3191

Difficulty: Medium

Language: 1class Solution {
2    public int minOperations(int[] nums) {
3        int count=0;
4        int k=3;
5        for(int i=0;i<nums.length;i++){
6            if(nums[i]==0){
7                if(i+2>=nums.length){
8                    return -1;
9                }
10                for(int j=i;j<k+i;j++){
11                    if(nums[j]==0) nums[j]=1;
12                    else nums[j]=0;
13                }
14                count++;
15            }
16        }
17        return count;
18    }
19}

Problem URL:
https://leetcode.com/problems/minimum-operations-to-make-binary-array-elements-equal-to-one-i/

Submission Date:
2026-08-05 14:49:35

Generated automatically by LeetSync.
