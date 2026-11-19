# Merge Sorted Array

Problem Number: 88

Difficulty: Easy

Language: 1class Solution {
2    public void merge(int[] nums1, int m, int[] nums2, int n) {
3        int i=m-1;
4        int j=n-1;
5        int k=nums1.length-1;
6        while(j>=0&&i>=0){
7            if(nums1[i]<nums2[j]){
8                nums1[k]=nums2[j];
9                j--;
10                k--;
11            }else{
12                nums1[k]=nums1[i];
13                k--;
14                i--;
15            }
16        }
17        //no need to consider nums1
18        while(j>=0){
19            nums1[k]=nums2[j];
20            j--;
21            k--;
22        }
23      
24    }
25}

Problem URL:
https://leetcode.com/problems/merge-sorted-array/

Submission Date:
2026-11-19 06:14:02

Generated automatically by LeetSync.
