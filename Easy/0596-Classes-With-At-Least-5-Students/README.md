# Classes With at Least 5 Students

Problem Number: 596

Difficulty: Easy

Language: 1# Write your MySQL query statement below
2select class
3from Courses
4group by class
5having count(student)>=5
6order by class;

Problem URL:
https://leetcode.com/problems/classes-with-at-least-5-students/

Submission Date:
2026-09-06 11:45:31

Generated automatically by LeetSync.
