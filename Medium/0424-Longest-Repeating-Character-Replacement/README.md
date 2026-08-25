# Longest Repeating Character Replacement

Problem Number: 424

Difficulty: Medium

Language: class Solution {
    public int characterReplacement(String s, int k) {
        int ans = 0;
        int n = s.length();
        for (char c = 'A'; c <= 'Z'; c++) {
            int i = 0, j = 0, replaced = 0;
            while (j < n) {
                if (s.charAt(j) == c) {
                    j++;
                } else if (replaced < k) {
                    j++;
                    replaced++;
                } else if (s.charAt(i) == c) {
                    i++;
                } else {
                    i++;
                    replaced--;
                }
                ans = Math.max(ans, j - i);
            }
        }
        return ans;
    }
}

Problem URL:
https://leetcode.com/problems/longest-repeating-character-replacement/

Submission Date:
2026-08-25 04:01:51

Generated automatically by LeetSync.
