# Valid Anagram

Problem Number: 242

Difficulty: Easy

Language: 1class Solution {
2    public boolean isAnagram(String s, String t) {
3        if(s.length()!=t.length()) return false;
4
5        int freq[]=new int[26];
6
7        for(int i=0;i<s.length();i++){
8            freq[s.charAt(i)-'a']++;
9            freq[t.charAt(i)-'a']--;
10        }
11
12        for(int i=0;i<26;i++){
13            if(freq[i]>0){
14                return false;
15            }
16        }
17        return true;
18    }
19}

Problem URL:
https://leetcode.com/problems/valid-anagram/

Submission Date:
2026-09-01 03:28:36

Generated automatically by LeetSync.
