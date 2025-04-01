## SQL Query Examples

### Ex.1. Select all fields and all rows
```sql
SELECT * FROM students;
```

### Ex.2. Select all student names from the table
```sql
SELECT name FROM students;
```

### Ex.3. Select only the user IDs
```sql
SELECT id FROM students;
```

### Ex.4. Select only user names
```sql
SELECT name FROM students;
```

### Ex.5. Select only user emails
```sql
SELECT email FROM students;
```

### Ex.6. Select user names and emails
```sql
SELECT name, email FROM students;
```

### Ex.7. Select user ID, name, email, and creation date
```sql
SELECT id, name, email, created_on FROM students;
```

### Ex.8. Select users with password '12333'
```sql
SELECT * FROM students
WHERE password = '12333';
```

### Ex.9. Select users created on '2021-03-26 00:00:00'
```sql
SELECT * FROM students
WHERE created_on = '2021-03-26 00:00:00';
```

### Ex.10. Select users whose name contains 'Anna'
```sql
SELECT * FROM students
WHERE name LIKE '%Anna%';
```

### Ex.11. Select users whose name ends with '8'
```sql
SELECT * FROM students
WHERE name LIKE '%8';
```

### Ex.12. Select users whose name contains the letter 'a'
```sql
SELECT * FROM students
WHERE name LIKE '%a%';
```

### Ex.13. Select users created on '2021-07-12 00:00:00'
```sql
SELECT * FROM students
WHERE created_on = '2021-07-12 00:00:00';
```

### Ex.14. Select users created on '2021-07-12 00:00:00' with password '1m313'
```sql
SELECT * FROM students
WHERE created_on = '2021-07-12 00:00:00' AND password = '1m313';
```

### Ex.15. Select users created on '2021-07-12 00:00:00' whose name contains 'Andrey'
```sql
SELECT * FROM students
WHERE created_on = '2021-07-12 00:00:00' AND name LIKE '%Andrey%';
```

### Ex.16. Select users created on '2021-07-12 00:00:00' whose name contains the digit '8'
```sql
SELECT * FROM students
WHERE created_on = '2021-07-12 00:00:00' AND name LIKE '%8%';
```

### Ex.17. Select the user with ID 110
```sql
SELECT * FROM students
WHERE id = 110;
```

### Ex.18. Select the user with ID 153
```sql
SELECT * FROM students
WHERE id = 153;
```

### Ex.19. Select users with ID greater than 140
```sql
SELECT * FROM students
WHERE id > 140;
```

### Ex.20. Select users with ID less than 130
```sql
SELECT * FROM students
WHERE id < 130;
```

### Ex.21. Select users with ID less than 127 or greater than 188
```sql
SELECT * FROM students
WHERE id < 127 OR id > 188;
```

### Ex.22. Select users with ID less than or equal to 137
```sql
SELECT * FROM students
WHERE id <= 137;
```

### Ex.23. Select users with ID greater than or equal to 137
```sql
SELECT * FROM students
WHERE id >= 137;
```

### Ex.24. Select users with ID greater than 180 but less than 190
```sql
SELECT * FROM students
WHERE id > 180 AND id < 190;
```

### Ex.25. Select users with ID between 180 and 190
```sql
SELECT * FROM students
WHERE id BETWEEN 180 AND 190;
```

### Ex.26. Select users with passwords '12333', '1m313', or '123313'
```sql
SELECT * FROM students
WHERE password IN ('12333', '1m313', '123313');
```

### Ex.27. Select users created on '2020-10-03 00:00:00', '2021-05-19 00:00:00', or '2021-03-26 00:00:00'
```sql
SELECT * FROM students
WHERE created_on IN ('2020-10-03 00:00:00', '2021-05-19 00:00:00', '2021-03-26 00:00:00');
```

### Ex.28. Select the minimum user ID
```sql
SELECT MIN(id) FROM students;
```

### Ex.29. Select the maximum user ID
```sql
SELECT MAX(id) FROM students;
```

### Ex.30. Select the total number of users
```sql
SELECT COUNT(id) FROM students;
```

### Ex.31. Select user ID, name, and creation date, ordered by ascending creation date
```sql
SELECT id, name, created_on FROM students
ORDER BY created_on;  -- Default order is ascending
```

### Ex.32. Select user ID, name, and creation date, ordered by descending creation date
```sql
SELECT id, name, created_on FROM students
ORDER BY created_on DESC;
```

---

## Join Examples

### Ex.33. Inner Join
```sql
SELECT students.id, students.name, courses.name
FROM students
INNER JOIN enrollments ON students.id = enrollments.student_id
INNER JOIN courses ON courses.id = enrollments.course_id;
```

### Ex.34. Left Join
```sql
SELECT students.id, students.name, courses.name
FROM students
LEFT JOIN enrollments ON students.id = enrollments.student_id
LEFT JOIN courses ON courses.id = enrollments.course_id;
```

### Ex.35. Right Join
```sql
SELECT students.id, students.name, courses.name
FROM students
RIGHT JOIN enrollments ON students.id = enrollments.student_id
RIGHT JOIN courses ON courses.id = enrollments.course_id;
```

### Ex.36. Full Outer Join
```sql
SELECT students.id, students.name, courses.name
FROM students
FULL OUTER JOIN enrollments ON students.id = enrollments.student_id
FULL OUTER JOIN courses ON courses.id = enrollments.course_id;
```

### Ex.37. Cross Join
```sql
SELECT students.id, students.name, courses.name
FROM students
CROSS JOIN courses;
```
