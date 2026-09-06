# Replace Employee ID With The Unique Identifier

Problem Number: 1378

Difficulty: Easy

Language: 1# Write your MySQL query statement below
2
3select uni.unique_id, e.name
4from Employees as e
5left join EmployeeUNI as uni
6on e.id=uni.id;

Problem URL:
https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/

Submission Date:
2026-09-06 05:58:27

Generated automatically by LeetSync.
