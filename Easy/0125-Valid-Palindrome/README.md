# Valid Palindrome

Problem Number: 125

Difficulty: Easy

Language: 1class Solution {
2    public boolean isPalindrome(String s) {
3
4        s = s.toLowerCase();
5        s = s.replaceAll("[^a-z0-9]", "");
6
7        String rev = "";
8
9        for (int i = s.length() - 1; i >= 0; i--) {
10            rev = rev + s.charAt(i);
11        }
12
13        return s.equals(rev);
14    }
15}

Problem URL:
https://leetcode.com/problems/valid-palindrome/

Submission Date:
2026-11-18 15:59:07

Generated automatically by LeetSync.
