# Longest Consecutive Sequence

Problem Number: 128

Difficulty: Medium

Language: 1class Solution {
2    public int longestConsecutive(int[] nums) {
3      HashSet<Integer> set=new HashSet<>();
4
5      for(int i=0;i<nums.length;i++){
6        set.add(nums[i]);
7      }
8
9      int longest=0;
10    ArrayList<Integer> list = new ArrayList<>(set);
11      for(int i=0;i<list.size();i++){
12
13         int num=list.get(i);
14
15         if(!set.contains(num-1)){
16            int current=num;
17            int count=1;
18
19            while(set.contains(current+1)){
20                current++;
21                count++;
22            }
23            longest=Math.max(longest,count);
24         }
25      }   
26      return longest;
27    }
28}

Problem URL:
https://leetcode.com/problems/longest-consecutive-sequence/

Submission Date:
2026-09-10 04:10:49

Generated automatically by LeetSync.
