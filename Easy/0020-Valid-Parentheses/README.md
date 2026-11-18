# Valid Parentheses

Problem Number: 20

Difficulty: Easy

Language: 1class Solution {
2    public boolean isValid(String s) {
3
4        while (s.contains("()") || s.contains("[]") || s.contains("{}")) {
5
6            s = s.replace("()", "");
7            s = s.replace("[]", "");
8            s = s.replace("{}", "");
9
10        }
11
12        return s.isEmpty();
13    }
14}

Problem URL:
https://leetcode.com/problems/valid-parentheses/

Submission Date:
2026-11-18 11:41:56

Generated automatically by LeetSync.
