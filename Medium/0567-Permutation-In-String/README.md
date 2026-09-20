# Permutation in String

Problem Number: 567

Difficulty: Medium

Language: 1class Solution {
2    public boolean checkInclusion(String s1, String s2) {
3        int need[]=new int[128];
4
5        for(int i=0;i<s1.length();i++){
6            need[s1.charAt(i)-'a']++;
7        }
8
9        int window[]=new int[128];
10
11        int left=0;
12        for(int right=0;right<s2.length();right++){
13            window[s2.charAt(right)-'a']++;
14
15            if(right-left+1>s1.length()){
16                window[s2.charAt(left)-'a']--;
17                left++;
18            }
19
20            if(right-left+1==s1.length()){
21                boolean flag=true;
22                for(int i=0;i<128;i++){
23                    if(need[i]!=window[i]){
24                        flag=false;
25                        break;
26                    }
27                }
28                if(flag){
29                    return true;
30                }
31            }
32
33        }
34        return false;
35    }
36}

Problem URL:
https://leetcode.com/problems/permutation-in-string/

Submission Date:
2026-09-20 16:04:07

Generated automatically by LeetSync.
