# Second Highest Salary

Problem Number: 176

Difficulty: Medium

Language: 1# Write your MySQL query statement below
2select max(salary) as SecondHighestSalary
3from Employee
4where salary <(
5    select max(salary)
6    from Employee
7);

Problem URL:
https://leetcode.com/problems/second-highest-salary/

Submission Date:
2026-11-19 05:19:19

Generated automatically by LeetSync.
