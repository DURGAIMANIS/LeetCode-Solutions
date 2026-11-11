# Valid Anagram

Problem Number: 242

Difficulty: Easy

Language: 1class Solution {
2    public boolean isAnagram(String s, String t) {
3        if(s.length()!=t.length()) return false;
4        //freq check
5        int count[]=new int[26];
6        //26 alphabet letters
7        // Time Complexity: O(n)
8        // Space Complexity: O(1)
9        for(int i=0;i<s.length();i++){
10            count[s.charAt(i)-'a']++;
11            count[t.charAt(i)-'a']--;
12        }
13        for(int i=0;i<26;i++){
14            if(count[i]!=0) return false;
15        }
16        return true;
17    }
18}

Problem URL:
https://leetcode.com/problems/valid-anagram/

Submission Date:
2026-11-11 02:02:30

Generated automatically by LeetSync.
