# Next Permutation

Problem Number: 31

Difficulty: Medium

Language: #include <vector>
#include <algorithm>
using namespace std;

class Solution {
public:
    void nextPermutation(vector<int>& nums) {
        int n = nums.size(), i = n - 2;
        
        // Step 1: Find the breakpoint
        while (i >= 0 && nums[i] >= nums[i + 1]) {
            i--;
        }
        
        if (i >= 0) {
            // Step 2: Find the smallest element larger than nums[i]
            int j = n - 1;
            while (nums[j] <= nums[i]) {
                j--;
            }
            swap(nums[i], nums[j]);
        }
        
        // Step 3: Reverse the subarray to the right of i
        reverse(nums.begin() + i + 1, nums.end());
    }
};

Problem URL:
https://leetcode.com/problems/next-permutation/

Submission Date:
2026-09-05 12:21:47

Generated automatically by LeetSync.
