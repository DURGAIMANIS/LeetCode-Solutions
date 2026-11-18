# Two Sum

Problem Number: 1

Difficulty: Easy

Language: 1class Solution {
2    public int[] twoSum(int[] nums, int target) {
3        HashMap<Integer,Integer> map=new HashMap<>();
4        for(int i=0;i<nums.length;i++){
5            int b=target-nums[i];
6            if(map.containsKey(b)){
7                return new int[]{i,map.get(b)};
8            }
9            map.put(nums[i],i);
10        }
11        return new int[]{};
12     }
13    
14}

Problem URL:
https://leetcode.com/problems/two-sum/

Submission Date:
2026-11-18 04:18:01

Generated automatically by LeetSync.
