# Rotate Image

Problem Number: 48

Difficulty: Medium

Language: 1class Solution {
2    public void rotate(int[][] matrix) {
3        int n=matrix.length;
4
5        //tranpose the matrix
6        for(int i=0;i<n;i++){
7            for(int j=i+1;j<n;j++){
8                int temp=matrix[i][j];
9                matrix[i][j]=matrix[j][i];
10                matrix[j][i]=temp;
11            }
12        }
13         
14         //swap two columns
15        for(int i=0;i<n;i++){
16            int left=0;
17            int right=n-1;
18
19            while(left<right){
20                int temp=matrix[i][left];
21                matrix[i][left]=matrix[i][right];
22                matrix[i][right]=temp;
23                left++;
24                right--;
25            }
26        }
27    }
28}

Problem URL:
https://leetcode.com/problems/rotate-image/

Submission Date:
2026-09-06 12:52:06

Generated automatically by LeetSync.
