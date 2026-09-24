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
14
15        if(n<0) a=n * -1;
16        else a=n;
17
18        double power=pow(x,a);
19
20        double answer=0;
21
22        if(n<0) answer = 1/power;
23        else answer=power;
24        
25        return answer;
26    }
27}

Problem URL:
https://leetcode.com/problems/powx-n/

Submission Date:
2026-09-24 02:03:28

Generated automatically by LeetSync.
