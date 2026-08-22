# Two Sum II - Input Array Is Sorted

Problem Number: 167

Difficulty: Medium

Language: 1class Solution {
2    public int[] twoSum(int[] numbers, int target) {
3        //array is sorted
4        //no need to use extra space
5        //time complexity is O(n)
6        int left=0;
7        int right=numbers.length-1;//5-4 =4 
8        while(left<right){
9            //don't use <= because we need two diff number
10            if((numbers[left]+numbers[right]) == target){
11                return new int[]{left+1,right+1};
12            }else if((numbers[left]+numbers[right])>target){
13                right--;
14            }else{
15                left++;
16            }
17        }
18        return new int[]{};
19    }
20}

Problem URL:
https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/

Submission Date:
2026-08-22 12:41:19

Generated automatically by LeetSync.
