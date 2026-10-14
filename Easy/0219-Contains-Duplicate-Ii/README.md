# Contains Duplicate II

Problem Number: 219

Difficulty: Easy

Language: 1class Solution {
2    public boolean containsNearbyDuplicate(int[] nums, int k) {
3       HashMap<Integer,Integer> hm=new HashMap<>();
4
5       for(int i=0;i<nums.length;i++){
6
7        if(!hm.containsKey(nums[i])){
8            hm.put(nums[i],i);
9        }else{
10            int pastindex=hm.get(nums[i]);
11            if(Math.abs(pastindex-i)<=k){
12                return true;
13            }else{
14                hm.put(nums[i],i);
15            }
16        }
17       } 
18
19       return false;
20    }
21}

Problem URL:
https://leetcode.com/problems/contains-duplicate-ii/

Submission Date:
2026-10-14 01:38:04

Generated automatically by LeetSync.
