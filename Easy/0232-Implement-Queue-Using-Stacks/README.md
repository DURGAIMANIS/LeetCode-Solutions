# Implement Queue using Stacks

Problem Number: 232

Difficulty: Easy

Language: 1class MyQueue {
2    Stack<Integer> stack1;
3    Stack<Integer> stack2;
4
5    public MyQueue() {
6        stack1=new Stack<>();
7        stack2=new Stack<>();
8    }
9    
10    public void push(int x) {
11        stack1.push(x);
12    }
13    
14    public int pop() {
15        if(stack2.isEmpty()){
16            while(!stack1.isEmpty()){
17                stack2.push(stack1.pop());
18            }
19        }
20        return stack2.pop();
21    }
22    
23    public int peek() {
24        if(stack2.isEmpty()){
25            while(!stack1.isEmpty()){
26                stack2.push(stack1.pop());
27            }
28        }
29        return stack2.peek();
30    }
31    
32    public boolean empty() {
33        return stack2.isEmpty() && stack1.isEmpty();
34    }
35}
36
37/**
38 * Your MyQueue object will be instantiated and called as such:
39 * MyQueue obj = new MyQueue();
40 * obj.push(x);
41 * int param_2 = obj.pop();
42 * int param_3 = obj.peek();
43 * boolean param_4 = obj.empty();
44 */

Problem URL:
https://leetcode.com/problems/implement-queue-using-stacks/

Submission Date:
2026-09-23 05:46:47

Generated automatically by LeetSync.
