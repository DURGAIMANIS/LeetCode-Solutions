# Longest Substring Without Repeating Characters

Problem Number: 3

Difficulty: Medium

Language: 1class Solution {
2    public int lengthOfLongestSubstring(String s) {
3
4        int left=0;
5        int max=0;
6
7        HashSet<Character> set=new HashSet<>();
8        for(int right=0;right<s.length();right++){
9            while(set.contains(s.charAt(right))){
10                set.remove(s.charAt(left));
11                left++;
12            }
13            set.add(s.charAt(right));
14            max=Math.max(max,(right-left)+1);
15        }
16        return max;
17    }
18}

Problem URL:
https://leetcode.com/problems/longest-substring-without-repeating-characters/

Submission Date:
2026-08-24 13:08:50

Generated automatically by LeetSync.
