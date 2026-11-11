# Reverse Words in a String

Problem Number: 151

Difficulty: Medium

Language: 1class Solution {
2    public String reverseWords(String s) {
3        // Time Complexity: O(n)
4        // Space Complexity: O(n)
5
6        String[] arr = s.trim().split("\\s+");
7        StringBuilder result = new StringBuilder();
8        for (int i=arr.length-1;i>=0;i--) {
9            result.append(arr[i]);
10            if (i!=0) {
11                result.append(" ");
12            }
13        }
14        return result.toString();
15    }
16}

Problem URL:
https://leetcode.com/problems/reverse-words-in-a-string/

Submission Date:
2026-11-11 02:09:57

Generated automatically by LeetSync.
