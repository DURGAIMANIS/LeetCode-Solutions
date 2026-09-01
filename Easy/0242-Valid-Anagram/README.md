# Valid Anagram

Problem Number: 242

Difficulty: Easy

Language: 1class Solution {
2    public boolean isAnagram(String s, String t) {
3        if(s.length()!=t.length()) return false;
4        //freq check
5        int count[]=new int[26];
6        //26 alphabet letters
7        for(int i=0;i<s.length();i++){
8            count[s.charAt(i)-'a']++;
9            count[t.charAt(i)-'a']--;
10        }
11        for(int i=0;i<26;i++){
12            if(count[i]!=0) return false;
13        }
14        return true;
15    }
16}

Problem URL:
https://leetcode.com/problems/valid-anagram/

Submission Date:
2026-09-01 03:31:26

Generated automatically by LeetSync.
