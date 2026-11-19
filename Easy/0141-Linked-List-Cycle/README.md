# Linked List Cycle

Problem Number: 141

Difficulty: Easy

Language: 1import java.util.HashSet;
2
3class Solution {
4    public boolean hasCycle(ListNode head) {
5
6        HashSet<ListNode> set = new HashSet<>();
7
8        ListNode temp = head;
9
10        while (temp != null) {
11
12            if (set.contains(temp)) {
13                return true;
14            }
15
16            set.add(temp);
17
18            temp = temp.next;
19        }
20
21        return false;
22    }
23}

Problem URL:
https://leetcode.com/problems/linked-list-cycle/

Submission Date:
2026-11-19 12:27:08

Generated automatically by LeetSync.
