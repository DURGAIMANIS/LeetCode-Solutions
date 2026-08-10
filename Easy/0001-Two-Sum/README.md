# Two Sum

Problem Number: 1

Difficulty: Easy

Language: 1class Solution {
2    public int[] twoSum(int[] nums, int target) {
3        
4        HashMap<Integer,Integer> map=new HashMap<>();
5        for(int i=0;i<nums.length;i++){
6            int remain=target-nums[i];
7            if(map.containsKey(remain)){
8                return new int[]{map.get(remain),i};
9            }
10            map.put(nums[i],i);
11        }
12        return new int[]{};
13    }
14    
15}

Problem URL:
https://leetcode.com/problems/two-sum/

Submission Date:
2026-08-10 06:02:19

Generated automatically by LeetSync.
