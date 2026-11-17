# Valid Anagram

Problem Number: 242

Difficulty: Easy

Language: 1class Solution {
2    public boolean isAnagram(String s, String t) {
3        if(s.length()!=t.length()){
4            return false;
5        }
6
7        int freq[]=new int[126];// capital and samll letters included, so 126
8
9        for(int i=0;i<s.length();i++){
10            freq[s.charAt(i)-'a']++;
11            freq[t.charAt(i)-'a']--;
12        }
13
14        for(int i=0;i<126;i++){
15            if(freq[i]!=0){
16                return false;
17            }
18        }
19        return true;
20    }
21}

Problem URL:
https://leetcode.com/problems/valid-anagram/

Submission Date:
2026-11-17 05:13:45

Generated automatically by LeetSync.
