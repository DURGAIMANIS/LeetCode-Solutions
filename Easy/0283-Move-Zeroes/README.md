# Move Zeroes

Problem Number: 283

Difficulty: Easy

Language: class Solution:
    def moveZeroes(self, nums):
        """
        :type nums: List[int]
        :rtype: void Do not return anything, modify nums in-place instead.
        """
        pos = 0
        
        for i in range(len(nums)):
            el = nums[i]
            if el != 0:
                nums[pos], nums[i] = nums[i], nums[pos]
                pos += 1

Problem URL:
https://leetcode.com/problems/move-zeroes/

Submission Date:
2026-08-10 06:43:44

Generated automatically by LeetSync.
