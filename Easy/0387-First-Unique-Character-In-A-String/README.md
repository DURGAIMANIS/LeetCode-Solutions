# First Unique Character in a String

Problem Number: 387

Difficulty: Easy

Language: 1class Solution {
2    public int firstUniqChar(String s) {
3        int freq[]=new int[126];
4        for(int i=0;i<s.length();i++){
5            freq[s.charAt(i)-'a']++;
6        }
7
8        for(int i=0;i<s.length();i++){
9            if(freq[s.charAt(i)-'a']==1){
10                return i;
11            }
12        }
13        return -1;
14    }
15}

Problem URL:
https://leetcode.com/problems/first-unique-character-in-a-string/

Submission Date:
2026-11-17 05:39:24

Generated automatically by LeetSync.
