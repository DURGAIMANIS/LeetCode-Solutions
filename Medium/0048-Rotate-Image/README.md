# Rotate Image

Problem Number: 48

Difficulty: Medium

Language: 1class Solution {
2    public void rotate(int[][] matrix) {
3        int n=matrix.length;
4
5        for(int i=0;i<n;i++){
6            for(int j=i+1;j<n;j++){
7                int temp=matrix[i][j];
8                matrix[i][j]=matrix[j][i];
9                matrix[j][i]=temp;
10            }
11        }
12
13        for(int i=0;i<n;i++){
14            int left=0;
15            int right=n-1;
16
17            while(left<right){
18                int temp=matrix[i][left];
19                matrix[i][left]=matrix[i][right];
20                matrix[i][right]=temp;
21                left++;
22                right--;
23            }
24        }
25    }
26}

Problem URL:
https://leetcode.com/problems/rotate-image/

Submission Date:
2026-09-02 02:53:37

Generated automatically by LeetSync.
