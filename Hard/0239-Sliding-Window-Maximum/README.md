# Sliding Window Maximum

Problem Number: 239

Difficulty: Hard

Language: 1class Solution {
2    public int[] maxSlidingWindow(int[] nums, int k) {
3        int n=nums.length;
4        int[] result=new int[n-k+1];
5        Deque<Integer> deque=new LinkedList<>();
6        for(int right=0;right<n;right++){
7            while(!deque.isEmpty()&&deque.peekFirst()<=right-k){
8                deque.pollFirst();
9            }
10            while(!deque.isEmpty()&&nums[deque.peekLast()]<nums[right]){
11               deque.pollLast();
12            }
13            deque.addLast(right);
14            if(right>=k-1){
15                result[right-k+1]=nums[deque.peekFirst()];
16            }
17        }
18        return result;
19    }
20}

Problem URL:
https://leetcode.com/problems/sliding-window-maximum/

Submission Date:
2026-09-28 04:48:53

Generated automatically by LeetSync.
