# Valid Parentheses

Problem Number: 20

Difficulty: Easy

Language: 1class Solution {
2    public boolean isValid(String s) {
3        int n=s.length();
4        Stack<Character> stack=new Stack<>();
5        for(int i=0;i<n;i++){
6           char ch=s.charAt(i);
7
8           if(ch=='('||ch=='['||ch=='{'){
9            stack.push(ch);
10           }else{
11            if(stack.isEmpty()) return false;
12            char top = stack.peek();
13
14            if((top == '[' && ch == ']') ||(top == '(' && ch == ')') ||(top == '{' && ch == '}')){
15                stack.pop();
16            }else{
17                return false;
18            }
19           }
20        }
21        return stack.isEmpty();
22    }
23}

Problem URL:
https://leetcode.com/problems/valid-parentheses/

Submission Date:
2026-09-23 02:10:04

Generated automatically by LeetSync.
