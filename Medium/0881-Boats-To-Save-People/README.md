# Boats to Save People

Problem Number: 881

Difficulty: Medium

Language: 1class Solution {
2    public int numRescueBoats(int[] people, int limit) {
3        int left =0;
4        int right=people.length-1;
5        int count=0;
6        Arrays.sort(people);
7
8        while(left<=right){
9            if(people[left]+people[right]<=limit){
10                left++;
11            }
12            right--;
13            count++;
14        }
15        return count;
16    }
17}

Problem URL:
https://leetcode.com/problems/boats-to-save-people/

Submission Date:
2026-10-14 05:05:28

Generated automatically by LeetSync.
