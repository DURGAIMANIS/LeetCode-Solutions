# 3Sum

Problem Number: 15

Difficulty: Medium

Language: 1class Solution {
2    public List<List<Integer>> threeSum(int[] nums) {
3        List<List<Integer>> res=new ArrayList<>();
4        Arrays.sort(nums);//return the values, not indexes;
5
6        for(int i=0;i<nums.length-2;i++){
7            if(i>0&&nums[i]==nums[i-1]) continue;//[1 1 1 3 4 6];
8
9            int j=i+1;//next value after i
10            int k=nums.length-1;//value of last array 
11
12            while(j<k){
13                int sum=nums[i]+nums[j]+nums[k];
14
15                if(sum==0){
16                    res.add(Arrays.asList(nums[i],nums[j],nums[k]));
17                    while(j<k && nums[j]==nums[j+1]) j++;
18                    while(j<k && nums[k]==nums[k-1]) k--;
19
20                    j++;//for no repeat same element for j
21                    k--;//for no repeat same element for k
22                }
23                else if(sum>0){
24                    k--;
25                }else{
26                    j++;
27                }
28            }
29        }
30        return res;
31        
32    }
33}

Problem URL:
https://leetcode.com/problems/3sum/

Submission Date:
2026-08-23 05:19:54

Generated automatically by LeetSync.
