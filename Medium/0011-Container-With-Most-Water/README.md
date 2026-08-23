# Container With Most Water

Problem Number: 11

Difficulty: Medium

Language: 1class Solution {
2    public int maxArea(int[] height) {
3        int left=0;
4        int right=height.length-1;
5
6        int maxArea=0;
7
8        while(left<right){
9            //it store the water in reactangular box,so we need lenght*base;
10            int length=Math.min(height[left],height[right]);
11            int base=right-left; //8-0 =8
12
13            int area=length*base;
14            maxArea=Math.max(maxArea,area);
15
16            if(height[left]<=height[right]) left++;//i need max water, so we need to hold greater value always
17            else right--;
18        }
19        return maxArea;
20    }
21}

Problem URL:
https://leetcode.com/problems/container-with-most-water/

Submission Date:
2026-08-23 05:36:21

Generated automatically by LeetSync.
