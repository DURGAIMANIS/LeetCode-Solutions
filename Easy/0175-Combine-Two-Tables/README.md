# Combine Two Tables

Problem Number: 175

Difficulty: Easy

Language: 1# Write your MySQL query statement below
2select p.firstName,p.lastName,a.city,a.state
3from Person p
4left join Address a
5on p.personId=a.personId;

Problem URL:
https://leetcode.com/problems/combine-two-tables/

Submission Date:
2026-11-11 03:23:39

Generated automatically by LeetSync.
