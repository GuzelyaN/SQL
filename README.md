# SQL  

This repository contains examples of SQL queries, including basic operations, various types of **JOINs** and examples from the projects.  

## 📌 Contents  

- [SQL Query Examples](https://github.com/GuzelyaN/SQL/blob/Overview/SQL%20Examples%20for%20Joins.md#sql-query-examples)  
  - Basic queries for retrieving, filtering, and sorting data.  
- [Join Examples](https://github.com/GuzelyaN/SQL/blob/Overview/SQL%20Examples%20for%20Joins.md#join-examples)  
  - Demonstrations of **INNER JOIN**, **LEFT JOIN**, **RIGHT JOIN**, and **FULL OUTER JOIN**.  

## 🚀 Thigers
select * from "AvatarTask" at2 where at2.updated_at > '2025-07-01' order by at2.updated_at ;
```
SELECT *, COUNT(*) OVER() AS total_count
FROM "AvatarTask" at2
WHERE at2."type" = 'BACKGROUND' 
  AND at2.updated_at > '2025-07-01' 
  AND at2.status = 'PROCESSING'
ORDER BY at2.updated_at;


SELECT *, COUNT(*) OVER() AS total_count
FROM "AvatarTask" at2
WHERE at2."type" = 'PERSONA' 
  AND at2.updated_at > '2025-07-01' 
  AND at2.status = 'PROCESSING'
ORDER BY at2.updated_at;

SELECT *, COUNT(*) OVER() AS total_count
FROM "AvatarTask" at2
WHERE at2."type" = 'COMBINE_2D' 
  AND at2.updated_at > '2025-07-01' 
  AND at2.status = 'PROCESSING'
ORDER BY at2.updated_at;

SELECT
  at2."type",
  COUNT(*) AS processing_count
FROM "AvatarTask" at2
WHERE at2.updated_at > '2025-07-01'
  AND at2.status = 'PROCESSING'
GROUP BY at2."type"
ORDER BY processing_count DESC;


SELECT COUNT(*) 
FROM "AvatarTask" at2 
WHERE at2."type" = 'BACKGROUND' 
  AND at2.updated_at > '2025-07-01' 
  AND at2.status = 'PROCESSING';







