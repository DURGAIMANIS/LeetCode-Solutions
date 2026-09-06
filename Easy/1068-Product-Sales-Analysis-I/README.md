# Product Sales Analysis I

Problem Number: 1068

Difficulty: Easy

Language: 1# Write your MySQL query statement below
2select p.product_name,s.year,s.price
3from Sales as s
4inner join Product as p
5on s.product_id=p.product_id;

Problem URL:
https://leetcode.com/problems/product-sales-analysis-i/

Submission Date:
2026-09-06 06:02:58

Generated automatically by LeetSync.
