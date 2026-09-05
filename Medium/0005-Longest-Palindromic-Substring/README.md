# Longest Palindromic Substring

Problem Number: 5

Difficulty: Medium

Language: 1class Solution {
2    public String longestPalindrome(String s) {
3
4        String answer="";
5
6        for(int i=0;i<s.length();i++){
7
8            String odd=expend(s,i,i);//odd char
9            String even=expend(s,i,i+1);
10
11            if(odd.length()>answer.length()){
12                answer=odd;
13            }
14            if(even.length()>answer.length()){
15                answer=even;
16            }
17        }
18        return answer;
19
20    }
21    public String expend(String s,int left,int right){
22        while(left>=0&&right<s.length()&&s.charAt(left)==s.charAt(right)){
23            left--;
24            right++;
25        }
26        return s.substring(left+1,right);
27    }
28}

Problem URL:
https://leetcode.com/problems/longest-palindromic-substring/

Submission Date:
2026-09-05 14:57:27

Generated automatically by LeetSync.
