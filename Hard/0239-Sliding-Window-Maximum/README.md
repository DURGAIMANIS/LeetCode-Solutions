# Sliding Window Maximum

Problem Number: 239

Difficulty: Hard

Language: 1class Solution {
2    public int[] maxSlidingWindow(int[] nums, int k) {
3        int n=nums.length;
4        
5        int result[]=new int[n-k+1];
6        Deque<Integer> deque=new LinkedList<>();
7
8        for(int right=0;right<n;right++){
9
10            while(!deque.isEmpty()&&deque.peekFirst()<=right-k){//remove from the first because of maintan the window 
11                deque.pollFirst();;
12            }
13            while(!deque.isEmpty()&&nums[deque.peekLast()]<nums[right]){
14                deque.pollLast();
15            }
16
17            deque.addLast(right);//stores the index
18            if(right>=k-1){
19                result[right-k+1]=nums[deque.peekFirst()];
20            }
21        }
22        return result;
23    }
24}

Problem URL:
https://leetcode.com/problems/sliding-window-maximum/

Submission Date:
2026-09-28 05:07:30

Generated automatically by LeetSync.
