# Majority Element

Problem Number: 169

Difficulty: Easy

Language: 1class Solution {
2    public int majorityElement(int[] nums) {
3       //Boyer-Moore Majority
4       int count=0;
5       int candidate=0;
6       for(int i=0;i<nums.length;i++){
7        if(count==0){
8            candidate=nums[i];
9        }
10        if(candidate==nums[i]){
11            count++;
12        }else{
13            count--;
14        }
15       }
16       return candidate;
17    }
18}

Problem URL:
https://leetcode.com/problems/majority-element/

Submission Date:
2026-09-06 13:37:55

Generated automatically by LeetSync.
