# Smallest Divisible Digit Product I

Problem Number: 3345

Difficulty: Easy

Language: 1class Solution {
2    public int smallestNumber(int n, int t) {
3        while(true){
4            int temp=n;
5            int ans=1;
6        while(temp>0){
7            int digit=temp%10;
8            ans*=digit;
9            temp/=10;
10        }
11        if(ans%t==0) return n;
12        else n=n+1;
13        }
14    }
15}

Problem URL:
https://leetcode.com/problems/smallest-divisible-digit-product-i/

Submission Date:
2026-08-06 04:14:06

Generated automatically by LeetSync.
