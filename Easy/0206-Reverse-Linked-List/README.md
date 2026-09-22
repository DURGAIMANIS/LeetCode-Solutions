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
13        ListNode prev=null;
14        ListNode temp=head;
15        
16        while(temp!=null){
17            ListNode next=temp.next;
18
19            temp.next=prev;
20            prev=temp;
21
22            temp=next;
23        }
24        return prev;
25    }
26}

Problem URL:
https://leetcode.com/problems/reverse-linked-list/

Submission Date:
2026-09-22 16:18:06

Generated automatically by LeetSync.
