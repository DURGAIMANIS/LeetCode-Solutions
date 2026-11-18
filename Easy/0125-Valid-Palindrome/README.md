# Valid Palindrome

Problem Number: 125

Difficulty: Easy

Language: 1class Solution {
2    public boolean isPalindrome(String s) {
3        int left=0;
4        int right=s.length()-1;
5        // Time Complexity: O(n)
6        // Space Complexity: O(1)
7        while(left<right){
8            if(!Character.isLetterOrDigit(s.charAt(left))){
9                left++;
10                continue;
11            }
12
13            if(!Character.isLetterOrDigit(s.charAt(right))){
14                right--;
15                continue;
16            }
17            char ch1=Character.toLowerCase(s.charAt(left));
18            char ch2=Character.toLowerCase(s.charAt(right));
19            if(ch1!=ch2){
20                return false;
21            }
22
23            left++;
24            right--;
25        }
26       return true;
27    }
28}

Problem URL:
https://leetcode.com/problems/valid-palindrome/

Submission Date:
2026-11-18 16:00:15

Generated automatically by LeetSync.
