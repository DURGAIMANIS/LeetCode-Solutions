# Best Time to Buy and Sell Stock

Problem Number: 121

Difficulty: Easy

Language: 1class Solution {
2    public int maxProfit(int[] prices) {
3        int max=0;
4        int min=prices[0];
5        // Time Complexity: O(n)
6        // Space Complexity: O(1)
7        for(int i=0;i<prices.length;i++){
8            if(prices[i]<min){
9                min=prices[i];
10            }
11            max=Math.max(max,prices[i]-min);
12        }
13        return max;
14    }
15}

Problem URL:
https://leetcode.com/problems/best-time-to-buy-and-sell-stock/

Submission Date:
2026-11-11 01:48:52

Generated automatically by LeetSync.
