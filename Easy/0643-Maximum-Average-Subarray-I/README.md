# Maximum Average Subarray I

Problem Number: 643

Difficulty: Easy

Language: class Solution {
    public double findMaxAverage(int[] nums, int k) {
        int n = nums.length;
        int sum = 0;
        for (int i = 0; i < k; i++) {
            sum += nums[i];
        }
        int maxSum = sum;
        for (int i = k; i < n; i++) {
            sum = sum - nums[i - k] + nums[i];
            if (sum > maxSum) {
                maxSum = sum;
            }
        }
        return (double) maxSum / k;
    }
}

Problem URL:
https://leetcode.com/problems/maximum-average-subarray-i/

Submission Date:
2026-09-18 09:50:38

Generated automatically by LeetSync.
