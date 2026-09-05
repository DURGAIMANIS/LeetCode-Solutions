# Group Anagrams

Problem Number: 49

Difficulty: Medium

Language: 1class Solution {
2    public List<List<String>> groupAnagrams(String[] strs) {
3
4        HashMap<String, List<String>> map=new HashMap<>();
5
6        for(int i=0;i<strs.length;i++){//pick one string
7            char[] word=strs[i].toCharArray();//convert it into char array
8            Arrays.sort(word);//sort the array
9            String key=new String(word);//make a string from the char array
10
11            if(!map.containsKey(key)){//check the key is present or not
12                map.put(key,new ArrayList<>());//if no, then put separate list for that
13            }
14            map.get(key).add(strs[i]);//otherwise, add the string at particular key
15        }
16        return new ArrayList<>(map.values());//return as ArrayList
17    }
18}

Problem URL:
https://leetcode.com/problems/group-anagrams/

Submission Date:
2026-09-05 13:00:00

Generated automatically by LeetSync.
