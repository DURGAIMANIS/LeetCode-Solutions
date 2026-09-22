# Binary Search

Problem Number: 704

Difficulty: Easy

Language: 1class Solution {
2
3    public int binary(int nums[],int target){
4        int l=0;
5        int r=nums.length-1;
6
7        while(l<=r){
8            int mid=l+(r-l)/2;
9            if(nums[mid]==target) return mid;
10            else if(nums[mid]<target) l=mid+1;
11            else r=mid-1;
12        }
13        return -1;
14    }
15
16    public int search(int[] nums, int target) {
17        return binary(nums,target);
18    }
19}

Problem URL:
https://leetcode.com/problems/binary-search/

Submission Date:
2026-09-22 01:44:05

Generated automatically by LeetSync.
