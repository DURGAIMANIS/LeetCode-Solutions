# Reverse Words in a String

Problem Number: 151

Difficulty: Medium

Language: class Solution {
    public String reverseWords(String s) {
        s = s.trim();
        String[] words = s.split("\\s+");
        Collections.reverse(Arrays.asList(words));
        return String.join(" ", words);
    }
}

Problem URL:
https://leetcode.com/problems/reverse-words-in-a-string/

Submission Date:
2026-09-05 12:40:18

Generated automatically by LeetSync.
