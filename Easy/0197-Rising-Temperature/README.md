# Rising Temperature

Problem Number: 197

Difficulty: Easy

Language: 1# Write your MySQL query statement below
2select current_day.id
3from Weather as current_day
4join Weather as previous_day
5on current_day.recordDate=DATE_ADD(previous_day.recordDate,INTERVAL 1 DAY)
6WHERE current_day.temperature>previous_day.temperature;

Problem URL:
https://leetcode.com/problems/rising-temperature/

Submission Date:
2026-09-06 06:54:42

Generated automatically by LeetSync.
