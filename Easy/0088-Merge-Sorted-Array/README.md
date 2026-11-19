# Merge Sorted Array

Problem Number: 88

Difficulty: Easy

Language: 1class Solution {
2    public void merge(int[] nums1, int m, int[] nums2, int n) {
3
4        int[] temp = new int[m + n];
5
6        // Copy nums1 elements
7        for (int i = 0; i < m; i++) {
8            temp[i] = nums1[i];
9        }
10
11        // Copy nums2 elements
12        for (int i = 0; i < n; i++) {
13            temp[m + i] = nums2[i];
14        }
15
16        // Sort the combined array
17        Arrays.sort(temp);
18
19        // Copy back to nums1
20        for (int i = 0; i < m + n; i++) {
21            nums1[i] = temp[i];
22        }
23    }
24}

Problem URL:
https://leetcode.com/problems/merge-sorted-array/

Submission Date:
2026-11-19 06:03:26

Generated automatically by LeetSync.
