# Valid Parentheses

Problem Number: 20

Difficulty: Easy

Language: 1class Solution {
2    public boolean isValid(String s) {
3        Stack<Character> stack=new Stack<>();
4        for(int i=0;i<s.length();i++){
5            char ch=s.charAt(i);
6            if(ch=='('||ch=='{'||ch=='['){
7                stack.push(ch);
8            }else{
9                if(stack.isEmpty()){
10                    return false;
11                }
12                if(    (stack.peek()=='('&&ch==')')
13                     ||(stack.peek()=='{'&&ch=='}')
14                     ||(stack.peek()=='['&&ch==']'))
15                {
16                    stack.pop();
17                }else{
18                    return false;
19                }
20            }
21        }
22        return stack.isEmpty();
23    }
24}

Problem URL:
https://leetcode.com/problems/valid-parentheses/

Submission Date:
2026-11-18 11:34:46

Generated automatically by LeetSync.
