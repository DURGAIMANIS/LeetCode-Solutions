# Spiral Matrix

Problem Number: 54

Difficulty: Medium

Language: 1class Solution {
2    public List<Integer> spiralOrder(int[][] matrix) {
3        int left=0;
4        int right=matrix[0].length-1;
5
6        int top=0;
7        int bottom=matrix.length-1;
8        
9        List<Integer> list=new ArrayList<>();
10
11        while(left<=right&&top<=bottom){
12            //left to right
13            for(int i=left;i<=right;i++){
14                list.add(matrix[top][i]);
15            }
16            top++;
17            //top to bottom
18
19            for(int i=top;i<=bottom;i++){
20                list.add(matrix[i][right]);
21            }
22
23            right--;
24
25            //right to left
26        if(top<=bottom){
27            for(int i=right;i>=left;i--){
28                list.add(matrix[bottom][i]);
29            }
30            bottom--;
31        }
32
33            //bottom to top
34        if(left<=right){
35            for(int i=bottom;i>=top;i--){
36                list.add(matrix[i][left]);
37            }
38            left++;
39        }
40        }
41        return list;
42    }
43}

Problem URL:
https://leetcode.com/problems/spiral-matrix/

Submission Date:
2026-09-06 12:53:41

Generated automatically by LeetSync.
