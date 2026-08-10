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
14        ListNode curr=head;
15        
16        while(curr!=null){
17            
18            ListNode next=curr.next;
19            
20            curr.next=prev;
21            prev=curr;
22            
23            curr=next;
24        }
25        return prev;
26        
27    }
28}

Problem URL:
https://leetcode.com/problems/reverse-linked-list/

Submission Date:
2026-08-10 17:18:47

Generated automatically by LeetSync.
