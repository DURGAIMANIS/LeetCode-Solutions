# Delete Duplicate Emails

Problem Number: 196

Difficulty: Easy

Language: 1# Write your MySQL query statement below
2delete p1
3from Person p1
4join Person p2
5on p1.email=p2.email
6where p1.id>p2.id;

Problem URL:
https://leetcode.com/problems/delete-duplicate-emails/

Submission Date:
2026-11-19 05:27:05

Generated automatically by LeetSync.
