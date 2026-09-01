# Valid Palindrome

Problem Number: 125

Difficulty: Easy

Language: 1class Solution {
2    public boolean isPalindrome(String s) {
3        int left=0;
4        int right=s.length()-1;
5        while(left<right){
6            if(!Character.isLetterOrDigit(s.charAt(left))){
7                left++;
8                continue;
9            }
10
11            if(!Character.isLetterOrDigit(s.charAt(right))){
12                right--;
13                continue;
14            }
15            char ch1=Character.toLowerCase(s.charAt(left));
16            char ch2=Character.toLowerCase(s.charAt(right));
17            if(ch1!=ch2){
18                return false;
19            }
20
21            left++;
22            right--;
23        }
24       return true;
25    }
26}

Problem URL:
https://leetcode.com/problems/valid-palindrome/

Submission Date:
2026-09-01 03:48:13

Generated automatically by LeetSync.
