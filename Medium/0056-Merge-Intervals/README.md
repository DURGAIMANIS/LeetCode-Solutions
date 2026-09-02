# Merge Intervals

Problem Number: 56

Difficulty: Medium

Language: 1import java.util.*;
2
3class Solution {
4    public int[][] merge(int[][] intervals) {
5        if (intervals.length <= 1) return intervals;
6
7        // Sort intervals by start time
8        Arrays.sort(intervals, (a, b) -> a[0] - b[0]);
9
10        List<int[]> merged = new ArrayList<>();
11        int[] current = intervals[0];
12
13        for (int i = 1; i < intervals.length; i++) {
14            if (intervals[i][0] <= current[1]) {
15                // Overlap, merge intervals
16                current[1] = Math.max(current[1], intervals[i][1]);
17            } else {
18                // No overlap, add current interval to list
19                merged.add(current);
20                current = intervals[i];
21            }
22        }
23        // Add the last interval
24        merged.add(current);
25
26        return merged.toArray(new int[merged.size()][]);
27    }
28}

Problem URL:
https://leetcode.com/problems/merge-intervals/

Submission Date:
2026-09-02 03:30:19

Generated automatically by LeetSync.
