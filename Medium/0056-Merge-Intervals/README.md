# Merge Intervals

Problem Number: 56

Difficulty: Medium

Language: 1class Solution {
2    public int[][] merge(int[][] intervals) {
3        //sort first 
4        Arrays.sort(intervals,(a,b) -> a[0]-b[0]);//sort ir based on the min difference
5
6        int[][] result=new int[intervals.length][2];
7        int resultIndex=0;
8
9        int currentStart=intervals[0][0];
10        int currentEnd=intervals[0][1];
11
12        for(int i=1;i<intervals.length;i++){
13
14            int nextStart=intervals[i][0];
15            int nextEnd=intervals[i][1];
16
17            if(nextStart<=currentEnd){
18                currentEnd=Math.max(currentEnd,nextEnd);
19            }
20            else{
21                result[resultIndex][0]=currentStart;
22                result[resultIndex][1]=currentEnd;
23
24                resultIndex++;
25
26                currentStart=nextStart;
27                currentEnd=nextEnd;
28            }
29        }
30
31        result[resultIndex][0]=currentStart;//last set
32        result[resultIndex][1]=currentEnd;
33
34        resultIndex++;
35        return Arrays.copyOf(result,resultIndex);
36    }
37}

Problem URL:
https://leetcode.com/problems/merge-intervals/

Submission Date:
2026-09-06 12:56:06

Generated automatically by LeetSync.
