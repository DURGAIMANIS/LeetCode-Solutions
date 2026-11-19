# List the Products Ordered in a Period

Problem Number: 1327

Difficulty: Easy

Language: SELECT p.product_name, SUM(o.unit) as unit
FROM Products p
JOIN Orders o
ON p.product_id = o.product_id
WHERE o.order_date LIKE '2020-02-%'
GROUP BY p.product_id
HAVING unit >= 100;

Problem URL:
https://leetcode.com/problems/list-the-products-ordered-in-a-period/

Submission Date:
2026-11-19 05:02:59

Generated automatically by LeetSync.
