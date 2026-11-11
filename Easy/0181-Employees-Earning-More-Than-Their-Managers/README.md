# Employees Earning More Than Their Managers

Problem Number: 181

Difficulty: Easy

Language: 1select e1.name as Employee
2from Employee e1
3join Employee e2
4on e1.managerId=e2.id
5where e1.salary>e2.salary;
6

Problem URL:
https://leetcode.com/problems/employees-earning-more-than-their-managers/

Submission Date:
2026-11-11 03:45:25

Generated automatically by LeetSync.
