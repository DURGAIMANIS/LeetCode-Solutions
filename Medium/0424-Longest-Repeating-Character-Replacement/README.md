# Longest Repeating Character Replacement

Problem Number: 424

Difficulty: Medium

Language: 1class Solution {
2    public int characterReplacement(String s, int k) {
3        int max=0;
4        int n=s.length();
5        for(char c='A';c<='Z';c++){
6            int left=0;
7            int right=0;
8            int replacement=0;
9            while(right<n){
10                if(s.charAt(right)==c){// chacrater is same as c
11                    right++;
12                }else if(replacement<k){//chacrater is not same,but we have replacement
13                    right++;
14                    replacement++;
15                }else if(s.charAt(left)==c){//no replacement, so delete first, but first may be sameas c
16                    left++;
17                }else{//no replcement, so delete first, but first may not be same as c
18                    left++;
19                    replacement--;
20                }
21                max=Math.max(max,right-left);// +1 not necessary, because right is already incraement by 1 
22            }
23        }
24        return max;
25    }
26}

Problem URL:
https://leetcode.com/problems/longest-repeating-character-replacement/

Submission Date:
2026-09-18 11:46:54

Generated automatically by LeetSync.
