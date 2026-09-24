# Pow(x, n)

Problem Number: 50

Difficulty: Medium

Language: 1class Solution {
2
3    public double pow(double x,long n){
4        if(n==0) return 1.0000;
5
6        double half=pow(x,n/2);
7
8        if(n%2==0) return half*half;
9        else return x*half*half;
10
11    }
12    public double myPow(double x, int n) {
13        long a=0;
14        if(n<0) a=n * -1;
15        else a=n;
16        double power=pow(x,a);
17        double answer=0;
18
19        if(n<0) answer = 1/power;
20        else answer=power;
21        return answer;
22    }
23}

Problem URL:
https://leetcode.com/problems/powx-n/

Submission Date:
2026-09-24 02:00:17

Generated automatically by LeetSync.
