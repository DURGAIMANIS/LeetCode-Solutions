# Substrings of Size Three with Distinct Characters

Problem Number: 1876

Difficulty: Easy

Language: 1class Solution {
2    public int countGoodSubstrings(String s) {
3        int k=2;
4        int count=0;
5        for(int i=0;i<s.length()-2;i++){
6            String result="";
7            for(int j=i;j<=k+i;j++){
8                result+=s.charAt(j);
9            }
10            char a = result.charAt(0);
11            char b = result.charAt(1);
12            char c = result.charAt(2);
13
14            if (a != b && b != c && a != c) {
15                count++;
16            }
17        }
18        return count;
19    }
20}

Problem URL:
https://leetcode.com/problems/substrings-of-size-three-with-distinct-characters/

Submission Date:
2026-08-05 16:21:18

Generated automatically by LeetSync.
