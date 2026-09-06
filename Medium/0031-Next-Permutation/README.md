# Next Permutation

Problem Number: 31

Difficulty: Medium

Language: 1class Solution {
2    public void nextPermutation(int[] nums) {
3        int n=nums.length;
4
5        int i=n-2;
6
7        while(i>=0&&nums[i]>=nums[i+1]){//find small value
8            i--;
9        }
10
11    if (i >= 0) {
12        int j=n-1;
13        while(nums[j]<=nums[i]){
14            j--;
15        }
16        int temp=nums[i];
17        nums[i]=nums[j];
18        nums[j]=temp;
19    }
20        reverse(nums,i+1,n-1);
21
22    }
23
24    public void reverse(int[] nums,int i,int j){
25        while(i<j){
26            int temp=nums[i];
27            nums[i]=nums[j];
28            nums[j]=temp;
29            i++;
30            j--;
31        }
32
33    }
34}

Problem URL:
https://leetcode.com/problems/next-permutation/

Submission Date:
2026-09-06 12:58:10

Generated automatically by LeetSync.
