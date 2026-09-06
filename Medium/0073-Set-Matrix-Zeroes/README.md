# Set Matrix Zeroes

Problem Number: 73

Difficulty: Medium

Language: 1class Solution {
2    public void setZeroes(int[][] matrix) {
3        int m=matrix.length;//row
4        int n=matrix[0].length;//col
5
6        boolean row[]=new boolean[m];
7        boolean col[]=new boolean[n];
8
9        for(int i=0;i<m;i++){
10            for(int j=0;j<n;j++){
11                if(matrix[i][j]==0){
12                    row[i]=true;
13                    col[j]=true;
14                }
15            }
16        }
17        
18        for(int i=0;i<m;i++){//row
19            if(row[i]){
20                for(int j=0;j<n;j++){
21                    matrix[i][j]=0;
22                }
23            }
24        }
25        for(int j=0;j<n;j++){//col
26            if(col[j]){
27                for(int i=0;i<m;i++){
28                    matrix[i][j]=0;
29                }
30            }
31        }
32    }
33}

Problem URL:
https://leetcode.com/problems/set-matrix-zeroes/

Submission Date:
2026-09-06 12:51:07

Generated automatically by LeetSync.
