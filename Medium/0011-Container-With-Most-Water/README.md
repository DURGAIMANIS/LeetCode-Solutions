# Container With Most Water

Problem Number: 11

Difficulty: Medium

Language: 1class Solution {
2    public int maxArea(int[] height) {
3        int left=0;
4        int right=height.length-1;
5        int maxarea=0;
6        while(left<right){
7
8            int h=Math.min(height[left],height[right]);//min decide how much store the water
9            int b=right-left; //right>left
10
11            int area=h*b;
12            maxarea=Math.max(maxarea,area);
13
14            if(height[left]<height[right]) left++;
15            else right--;
16        }
17        return maxarea;
18    }
19}

Problem URL:
https://leetcode.com/problems/container-with-most-water/

Submission Date:
2026-08-23 06:02:53

Generated automatically by LeetSync.
