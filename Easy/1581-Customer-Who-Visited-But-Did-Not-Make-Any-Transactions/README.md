# Customer Who Visited but Did Not Make Any Transactions

Problem Number: 1581

Difficulty: Easy

Language: 1select v.customer_id,COUNT(*) AS count_no_trans
2from Visits v
3left join Transactions s # left join, because visitors , but no need to trans
4on v.visit_id=s.visit_id
5where transaction_id is null # no transaction in 1st condition
6group by v.customer_id; # count the customer visit

Problem URL:
https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/

Submission Date:
2026-11-11 04:16:05

Generated automatically by LeetSync.
