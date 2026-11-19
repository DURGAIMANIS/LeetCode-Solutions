# Reverse Linked List

Problem Number: 206

Difficulty: Easy

Language: 1/**
2 * Definition for singly-linked list.
3 * public class ListNode {
4 *     int val;
5 *     ListNode next;
6 *     ListNode() {}
7 *     ListNode(int val) { this.val = val; }
8 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
9 * }
10 */
11class Solution {
12    public ListNode reverseList(ListNode head) {
13        ListNode newlist=null;
14        ListNode temp=head;
15        while(temp!=null){
16            ListNode nextlist=temp.next;
17            temp.next=newlist;
18            newlist=temp;
19            temp=nextlist;
20        }
21        return newlist;
22    }
23}

Problem URL:
https://leetcode.com/problems/reverse-linked-list/

Submission Date:
2026-11-19 12:08:35

Generated automatically by LeetSync.
