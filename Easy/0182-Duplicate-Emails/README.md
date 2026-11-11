# Duplicate Emails

Problem Number: 182

Difficulty: Easy

Language: 1select email
2from Person
3group by email
4having count(email)>1;

Problem URL:
https://leetcode.com/problems/duplicate-emails/

Submission Date:
2026-11-11 03:39:08

Generated automatically by LeetSync.
