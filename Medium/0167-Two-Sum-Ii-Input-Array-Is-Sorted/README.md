# Two Sum II - Input Array Is Sorted

Problem Number: 167

Difficulty: Medium

Language: 1class Solution {
2    public int[] twoSum(int[] numbers, int target) {
3        //array is sorted
4        //no need to use extra space
5        int left=0;
6        int right=numbers.length-1;//5-4 =4 
7        while(left<right){
8            //don't use <= because we need two diff number
9            if((numbers[left]+numbers[right]) == target){
10                return new int[]{left+1,right+1};
11            }else if((numbers[left]+numbers[right])>target){
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
2026-08-22 12:35:08

Generated automatically by LeetSync.
