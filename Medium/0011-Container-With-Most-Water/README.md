# Container With Most Water

Problem Number: 11

Difficulty: Medium

Language: 1class Solution {
2    public int maxArea(int[] height) {
3        int left=0;
4        int right=height.length-1;
5
6        int maxarea=0;
7        while(left<right){
8
9            int h=Math.min(height[left],height[right]);//min decide how much store the water
10            int b=right-left; //right>left
11
12            int area=h*b;
13            maxarea=Math.max(maxarea,area);
14
15            if(height[left]<height[right]) left++;
16            else right--;
17        }
18        return maxarea;
19    }
20}

Problem URL:
https://leetcode.com/problems/container-with-most-water/

Submission Date:
2026-08-23 05:59:50

Generated automatically by LeetSync.
