# Merge Two Sorted Lists

Problem Number: 21

Difficulty: Easy

Language: 1
2class Solution {
3    public ListNode mergeTwoLists(ListNode list1, ListNode list2) {
4
5        ListNode dummy = new ListNode(0);
6        ListNode current = dummy;
7
8        while (list1 != null && list2 != null) {
9
10            if (list1.val <= list2.val) {
11                current.next = list1;
12                list1 = list1.next;
13            }
14            else {
15                current.next = list2;
16                list2 = list2.next;
17            }
18
19            current = current.next;
20        }
21
22        if (list1 != null) {
23            current.next = list1;
24        }
25
26        if (list2 != null) {
27            current.next = list2;
28        }
29
30        return dummy.next;
31    }
32}
33

Problem URL:
https://leetcode.com/problems/merge-two-sorted-lists/

Submission Date:
2026-11-24 14:50:03

Generated automatically by LeetSync.
