# Palindromic Substrings

Problem Number: 647

Difficulty: Medium

Language: 1class Solution {
2    public int countSubstrings(String s) {
3
4        int count=0;
5
6        for(int i=0;i<s.length();i++){
7            count+=expend(s,i,i);//odd char
8            count+=expend(s,i,i+1);
9
10        }
11        return count;
12
13    }
14    public int expend(String s,int left,int right){
15        int count=0;
16        while(left>=0&&right<s.length()&&s.charAt(left)==s.charAt(right)){
17            count++;
18            left--;
19            right++;
20        }
21        return count;
22    }
23}

Problem URL:
https://leetcode.com/problems/palindromic-substrings/

Submission Date:
2026-09-05 15:01:40

Generated automatically by LeetSync.
