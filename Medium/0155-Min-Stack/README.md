# Min Stack

Problem Number: 155

Difficulty: Medium

Language: 1class MinStack {
2    Stack<Integer> stack;
3    Stack<Integer> minStack;
4
5    public MinStack() {
6        stack = new Stack<>();
7        minStack = new Stack<>();
8    }
9
10    public void push(int val) {
11        stack.push(val);
12
13        if (minStack.isEmpty() || val <= minStack.peek()) {
14            minStack.push(val);
15        } else {
16            minStack.push(minStack.peek());
17        }
18    }
19
20    public void pop() {
21        stack.pop();
22        minStack.pop();
23    }
24
25    public int top() {
26        return stack.peek();
27    }
28
29    public int getMin() {
30        return minStack.peek();
31    }
32}

Problem URL:
https://leetcode.com/problems/min-stack/

Submission Date:
2026-11-19 12:50:38

Generated automatically by LeetSync.
