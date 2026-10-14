# Longest Substring Without Repeating Characters

Problem Number: 3

Difficulty: Medium

Language: 1class Solution {
2    public int lengthOfLongestSubstring(String s) {
3        int max=0;
4        int left=0;
5        int right=0;
6        HashSet<Character> set=new HashSet<>();
7        while(right<s.length()){
8            while(set.contains(s.charAt(right))){
9                set.remove(s.charAt(left));
10                left++;
11            }
12            set.add(s.charAt(right));
13            
14            int length=right-left+1;
15            max=Math.max(max,length);
16            right++;
17        }
18        return max;
19        
20    }
21}
22/*
23import java.util.*;
24
25class Solution {
26    public int lengthOfLongestSubstring(String s) {
27        int max = 0;
28        int left = 0;
29
30        HashSet<Character> set = new HashSet<>();
31
32        for (int right = 0; right < s.length(); right++) {
33            while (set.contains(s.charAt(right))) {
34                set.remove(s.charAt(left));
35                left++;
36            }
37
38            set.add(s.charAt(right));
39
40            int length = right - left + 1;
41            max = Math.max(max, length);
42        }
43
44        return max;
45    }
46}*/

Problem URL:
https://leetcode.com/problems/longest-substring-without-repeating-characters/

Submission Date:
2026-10-14 05:14:22

Generated automatically by LeetSync.
