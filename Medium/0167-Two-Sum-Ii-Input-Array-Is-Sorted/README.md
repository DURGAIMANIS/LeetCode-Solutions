# Two Sum II - Input Array Is Sorted

Problem Number: 167

Difficulty: Medium

Language: 1class Solution {
2    public int[] twoSum(int[] numbers, int target) {
3        int left=0;
4        int sum=0;
5        int right=numbers.length-1;
6
7        while(left<right){
8            sum=numbers[left]+numbers[right];
9            if(sum==target){
10                return new int[]{left+1,right+1};
11            }else if(sum>target){
12                right--;
13            }else{
14                left++;
15            }
16        }
17        return new int[]{};
18    }
19}

Problem URL:
https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/

Submission Date:
2026-11-18 11:39:49

Generated automatically by LeetSync.
