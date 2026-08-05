# Longest Substring Without Repeating Characters

Problem Number: 3

Difficulty: Medium

Language: 1class Solution {
2    public int lengthOfLongestSubstring(String s) {
3        HashSet<Character> seen=new HashSet<>();
4
5        int start=0;
6        int end=0;
7        int maxlen=0;
8
9        while(end<s.length()){
10            char c=s.charAt(end);
11
12            while(seen.contains(c)){
13                seen.remove(s.charAt(start));
14                start+=1;
15            }
16            seen.add(c);
17
18            int window=end-start+1;
19
20            maxlen=Math.max(maxlen,window);
21            end+=1;
22        }
23        return maxlen;
24    }
25}

Problem URL:
https://leetcode.com/problems/longest-substring-without-repeating-characters/

Submission Date:
2026-08-05 12:17:36

Generated automatically by LeetSync.
