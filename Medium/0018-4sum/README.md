# 4Sum

Problem Number: 18

Difficulty: Medium

Language: 1class Solution {
2    public List<List<Integer>> fourSum(int[] nums, int target) {
3        List<List<Integer>> result=new ArrayList<>();
4
5        Arrays.sort(nums);
6
7        for(int i=0;i<nums.length;i++){//for first element
8            if(i>0&&nums[i]==nums[i-1]){
9                continue;
10            }
11
12            for(int j=i+1;j<nums.length;j++){//for second element
13                if(j>i+1&&nums[j]==nums[j-1]){
14                    continue;
15                }
16
17                int left=j+1;//for 3rd element
18                int right=nums.length-1;//for 4th element
19
20                while(left<right){
21                    long sum= (long)nums[i]+nums[j]+nums[left]+nums[right];
22                    if(sum==target){
23                        result.add(Arrays.asList(nums[i],nums[j],nums[left],nums[right]));
24
25                        while(left<right&&nums[left]==nums[left+1]){
26                            left++;
27                        }
28
29                        while(left<right&&nums[right]==nums[right-1]){
30                            right--;
31                        }
32
33                        left++;
34                        right--;
35                    }
36                    else if(sum<target){
37                        left++;
38                    }else{
39                        right--;
40                    }
41                }
42            }
43        }
44        return result;
45    }
46}

Problem URL:
https://leetcode.com/problems/4sum/

Submission Date:
2026-09-18 11:42:17

Generated automatically by LeetSync.
