# Majority Element

Problem Number: 169

Difficulty: Easy

Language: 1class Solution {
2    public int majorityElement(int[] nums) {
3       //Boyer-Moore Majority
4       int count=0;
5       int candidate=0;
6
7       for(int i=0;i<nums.length;i++){
8        if(count==0){
9            candidate=nums[i];
10        }
11
12        if(candidate==nums[i]){
13            count++;
14        }else{
15            count--;
16        }
17       }
18       return candidate;
19    }
20}

Problem URL:
https://leetcode.com/problems/majority-element/

Submission Date:
2026-09-06 13:51:18

Generated automatically by LeetSync.
