# Top K Frequent Elements

Problem Number: 347

Difficulty: Medium

Language: 1class Solution {
2    public int[] topKFrequent(int[] nums, int k) {
3        HashMap<Integer,Integer> map=new HashMap<>();
4
5        for(int i=0;i<nums.length;i++){
6            if(map.containsKey(nums[i])){
7                map.put(nums[i],map.get(nums[i])+1);
8            }else{
9                map.put(nums[i],1);
10            }
11        }
12
13        ArrayList<Integer> list=new ArrayList<>(map.keySet());
14
15        Collections.sort(list, (a,b)-> map.get(b)-map.get(a));
16
17        int arr[]=new int[k];
18
19        for(int i=0;i<k;i++){
20            arr[i]=list.get(i);
21        }
22        return arr;
23    }
24}

Problem URL:
https://leetcode.com/problems/top-k-frequent-elements/

Submission Date:
2026-09-10 03:21:07

Generated automatically by LeetSync.
