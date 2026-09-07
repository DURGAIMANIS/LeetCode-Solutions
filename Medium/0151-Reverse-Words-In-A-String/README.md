# Reverse Words in a String

Problem Number: 151

Difficulty: Medium

Language: 1class Solution {
2    public String reverseWords(String s) {
3        String arr[]=s.trim().split("\\s+");
4
5        String result="";
6        for(int i=arr.length-1;i>=0;i--){
7            result+=arr[i];
8            if(i!=0){
9                result+=" ";
10            }
11        }
12        return result;
13        
14    }
15}

Problem URL:
https://leetcode.com/problems/reverse-words-in-a-string/

Submission Date:
2026-09-07 03:50:46

Generated automatically by LeetSync.
