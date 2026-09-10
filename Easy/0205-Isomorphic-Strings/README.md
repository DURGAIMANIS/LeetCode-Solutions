# Isomorphic Strings

Problem Number: 205

Difficulty: Easy

Language: 1class Solution {
2    public boolean isIsomorphic(String s, String t) {
3        if(s.length()!=t.length()) return false;
4
5        HashMap<Character,Character> map1=new HashMap<>();
6        HashMap<Character,Character> map2=new HashMap<>();
7        for(int i=0;i<s.length();i++){
8
9            char a=s.charAt(i);
10            char b=t.charAt(i);
11
12            if(map1.containsKey(a)&&map1.get(a)!=b){
13                return false;
14            }
15
16            if(map2.containsKey(b)&&map2.get(b)!=a){
17                return false;
18            }
19
20            map1.put(a,b);
21            map2.put(b,a);
22
23        }
24        return true;
25
26    }
27}

Problem URL:
https://leetcode.com/problems/isomorphic-strings/

Submission Date:
2026-09-10 10:17:00

Generated automatically by LeetSync.
