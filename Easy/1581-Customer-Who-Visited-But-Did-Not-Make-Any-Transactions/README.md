# Customer Who Visited but Did Not Make Any Transactions

Problem Number: 1581

Difficulty: Easy

Language: 1# Write your MySQL query statement below
2
3select v.customer_id, COUNT(*) as count_no_trans
4from Visits as v
5where v.visit_id not in(
6  select t.visit_id from Transactions as t
7)
8GROUP BY v.customer_id;

Problem URL:
https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/

Submission Date:
2026-09-06 06:20:16

Generated automatically by LeetSync.
