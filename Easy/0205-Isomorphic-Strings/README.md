# Isomorphic Strings

Problem Number: 205

Difficulty: Easy

Language: 1class Solution {
2    public boolean isIsomorphic(String s, String t) {
3        int[] map1 = new int[256];
4        int[] map2 = new int[256];
5
6        for (int i = 0; i < s.length(); i++) {
7            char a = s.charAt(i);
8            char b = t.charAt(i);
9
10            if (map1[a] != map2[b]) {
11                return false;
12            }
13
14            map1[a] = i + 1;
15            map2[b] = i + 1;
16        }
17
18        return true;
19    }
20}

Problem URL:
https://leetcode.com/problems/isomorphic-strings/

Submission Date:
2026-11-18 16:33:25

Generated automatically by LeetSync.
