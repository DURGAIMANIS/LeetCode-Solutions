# Search in Rotated Sorted Array

Problem Number: 33

Difficulty: Medium

Language: 1class Solution {
2    public int search(int[] nums, int target) {
3        //we can use linear search
4        int low=0;
5        int high=nums.length-1;
6        while(low<=high){
7            int mid=low+(high-low) / 2;
8            if(target==nums[mid]){
9                return mid;
10            }
11            if(nums[low] <= nums[mid]){
12                if(nums[low]<=target&&target<nums[mid]){
13                    high=mid-1;
14                }else{
15                    low=mid+1;
16                }
17            }
18            else if(nums[mid]<=nums[high]){
19                if(nums[mid]<target&&target<=nums[high]){
20                    low=mid+1;
21                }else{
22                    high=mid-1;
23                }
24            }
25        }
26        return -1;
27    }
28}

Problem URL:
https://leetcode.com/problems/search-in-rotated-sorted-array/

Submission Date:
2026-11-19 06:37:23

Generated automatically by LeetSync.
