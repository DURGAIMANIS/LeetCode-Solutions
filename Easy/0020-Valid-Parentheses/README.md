# Valid Parentheses

Problem Number: 20

Difficulty: Easy

Language: 1class Solution {
2    public boolean isValid(String s) {
3        while(s.contains("()")||s.contains("[]")||s.contains("{}")){
4            s=s.replace("()","");
5            s=s.replace("{}","");
6            s=s.replace("[]","");
7        }
8        return s=="";
9    }
10}

Problem URL:
https://leetcode.com/problems/valid-parentheses/

Submission Date:
2026-11-18 11:15:28

Generated automatically by LeetSync.
