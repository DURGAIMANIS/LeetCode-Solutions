# Longest Common Prefix

Problem Number: 14

Difficulty: Easy

Language: 1class Solution {
2    public String longestCommonPrefix(String[] strs) {
3        String prefix=strs[0];
4
5        for(int i=1;i<strs.length;i++){
6            while(strs[i].startsWith(prefix)==false){
7                prefix=prefix.substring(0,prefix.length()-1);
8            }
9        }
10        return prefix;
11    }
12}

Problem URL:
https://leetcode.com/problems/longest-common-prefix/

Submission Date:
2026-09-05 12:46:47

Generated automatically by LeetSync.
