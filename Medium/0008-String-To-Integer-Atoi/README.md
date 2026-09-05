# String to Integer (atoi)

Problem Number: 8

Difficulty: Medium

Language: 1class Solution {
2    public int myAtoi(String s) {
3        //ignore the space
4        int i=0;
5        while(i<s.length()&&s.charAt(i)==' '){
6            i++;
7        }
8
9        //check the sign(+ or -)
10        int sign=1;
11        if(i<s.length()&&s.charAt(i)=='-'){
12            sign=-1;
13            i++;
14        }else if (i < s.length() && s.charAt(i) == '+'){
15            i++;
16        }
17
18        //read the digit
19        int result=0;
20        while(i<s.length()&&Character.isDigit(s.charAt(i))){
21            int digit=s.charAt(i)-'0';//give string as int("4" to 4)
22            // 4. Check overflow
23            if (result > (Integer.MAX_VALUE - digit) / 10) {
24                if (sign == 1) {
25                    return Integer.MAX_VALUE;
26                } else {
27                    return Integer.MIN_VALUE;
28                }
29            }
30            result=result*10+digit;
31            i++;
32        }
33        return result*sign;
34    }
35}

Problem URL:
https://leetcode.com/problems/string-to-integer-atoi/

Submission Date:
2026-09-05 13:17:59

Generated automatically by LeetSync.
