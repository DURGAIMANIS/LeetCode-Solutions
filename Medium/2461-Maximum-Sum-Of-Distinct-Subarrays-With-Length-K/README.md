# Maximum Sum of Distinct Subarrays With Length K

Problem Number: 2461

Difficulty: Medium

Language: public long maximumSubarraySum(int[] nums, int k) {
    long sum = 0;
    long curr = 0;
    int i =0;
    int j =0;
    Set<Integer> set = new HashSet<>();
    while(j<nums.length){
        while(set.size()==k ||  set.contains(nums[j])){
            set.remove(nums[i]);
            curr -= nums[i++];
        }
        set.add(nums[j]);
        curr += nums[j++];
        if(set.size()==k){
            sum = Math.max(sum, curr);
        }
    }
    return sum;
}

Problem URL:
https://leetcode.com/problems/maximum-sum-of-distinct-subarrays-with-length-k/

Submission Date:
2026-08-23 09:27:20

Generated automatically by LeetSync.
