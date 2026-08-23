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
10            int sum=(numbers[left]+numbers[right]) ;
11            if(sum == target){
12                return new int[]{left+1,right+1};
13            }else if(sum>target){
14                right--;
15            }else{
16                left++;
17            }
18        }
19        return new int[]{};
20    }
21}

Problem URL:
https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/

Submission Date:
2026-08-23 05:16:00

Generated automatically by LeetSync.
