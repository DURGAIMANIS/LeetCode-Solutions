# Find Users With Valid E-Mails

Problem Number: 1517

Difficulty: Easy

Language: 1SELECT *
2FROM Users
3WHERE REGEXP_LIKE(
4    mail,
5    '^[A-Za-z][A-Za-z0-9_.-]*@leetcode[.]com$',
6    'c'
7);

Problem URL:
https://leetcode.com/problems/find-users-with-valid-e-mails/

Submission Date:
2026-11-18 17:38:27

Generated automatically by LeetSync.
