# Two Sum II - Input Array Is Sorted

Problem Number: 167

Difficulty: Medium

Language: 1import java.util.HashMap;
2
3class Solution {
4    public int[] twoSum(int[] numbers, int target) {
5
6        HashMap<Integer, Integer> map = new HashMap<>();
7
8        for (int i = 0; i < numbers.length; i++) {
9
10            int b = target - numbers[i];
11
12            if (map.containsKey(b)) {
13                return new int[]{map.get(b) + 1, i + 1};
14            }
15
16            map.put(numbers[i], i);
17        }
18
19        return new int[]{};
20    }
21}

Problem URL:
https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/

Submission Date:
2026-11-18 12:02:07

Generated automatically by LeetSync.
