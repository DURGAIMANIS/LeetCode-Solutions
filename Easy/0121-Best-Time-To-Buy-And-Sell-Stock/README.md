# Best Time to Buy and Sell Stock

Problem Number: 121

Difficulty: Easy

Language: 1class Solution {
2    public int maxProfit(int[] prices) {
3        int max=0;
4        int min=prices[0];
5        for(int i=0;i<prices.length;i++){
6              if(prices[i]<min){
7                min=prices[i];
8              }else{
9                max=Math.max(max,prices[i]-min);
10
11              }
12        }
13        return max;
14    }
15}

Problem URL:
https://leetcode.com/problems/best-time-to-buy-and-sell-stock/

Submission Date:
2026-08-10 06:13:52

Generated automatically by LeetSync.
