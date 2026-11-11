# Replace Employee ID With The Unique Identifier

Problem Number: 1378

Difficulty: Easy

Language: 1select u.unique_id,e.name
2from Employees e
3left join EmployeeUNI u
4on e.id=u.id;

Problem URL:
https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/

Submission Date:
2026-11-11 03:58:18

Generated automatically by LeetSync.
