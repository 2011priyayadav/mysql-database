## What is SQL?
1. SQL stands for Structured Query Language
2. SQL lets you access and manipulate databases
3. SQL became a standard of the American National Standards Institute (ANSI) in 1986, and of the International Organization for Standardization (ISO) in 1987

# Some of The Most Important SQL Commands
SELECT - extracts data from a database
UPDATE - updates data in a database
DELETE - deletes data from a database
INSERT INTO - inserts new data into a database
CREATE DATABASE - creates a new database
ALTER DATABASE - modifies a database
CREATE TABLE - creates a new table
ALTER TABLE - modifies a table
DROP TABLE - deletes a table
CREATE INDEX - creates an index (search key)
DROP INDEX - deletes an index



# mysql-database







## SELECT QUERY Guide
This document explains SQL SELECT queries step-by-step with keywords, clauses, conditions, and examples. It is written in plain format for learning, revision, or adding to a GitHub README.

---

## 1. SELECT — Basic Keyword

**Used to fetch data from a table.**

```sql
SELECT column1, column2 FROM table_name;
```

**Example:**

```sql
SELECT name, age FROM students;
```

---

## 2. SELECT \* — Select All Columns

```sql
SELECT * FROM students;
```

*Get all data from the students table.*

---

## 3. WHERE — Filter Rows

```sql
SELECT * FROM students WHERE age > 18;
```

*Get students older than 18.*

---

## 4. AND(&&), OR(||), NOT(!=) — Combine Conditions

**AND(&&):**

```sql
SELECT * FROM students WHERE age > 18 AND gender = 'Female';
```
```sql
SELECT * FROM students WHERE age > 18 && gender = 'Female';
```

**OR(||):**

```sql
SELECT * FROM students WHERE course = 'BCA' OR course = 'MBA';
```
```sql
SELECT * FROM students WHERE course = 'BCA' || course = 'MBA';
```

**NOT(!=):**

```sql
SELECT * FROM students WHERE NOT gender = 'Male';
```
```sql
SELECT * FROM students WHERE gender != 'Male';
```
---

## 5. ORDER BY — Sort the Results

**Ascending Order:**

```sql
SELECT * FROM students ORDER BY age ASC;
```

**Descending Order:**

```sql
SELECT * FROM students ORDER BY name DESC;
```

---

## 6. LIMIT — Restrict Number of Rows (Offest, total records value)
```sql
SELECT * FROM students LIMIT 2, 5;
```
*LIMIT 2, 5 means 2 is offset which start row with 3 and 5 is total number of records get from table.*
*Offset always start with 0 so suppose if we have offset 2 then it will start with 3 row*

```sql
SELECT * FROM students LIMIT 3;
```

*Show only the first 3 students.*

---

## 7. LIKE — Pattern Matching

**Starts with 'P':**

```sql
SELECT * FROM students WHERE name LIKE 'P%';
```

**Ends with 'ya':**

```sql
SELECT * FROM students WHERE name LIKE '%ya';
```

**Search where name and department must have i from employee table**
```sql
SELECT * FROM `testDB`.`employees` where name like '%i%' or department like '%i%';
```

---

## 8. IN — Match Multiple Values

```sql
SELECT * FROM students WHERE course IN ('BCA', 'BBA');
```

---

## 9. BETWEEN — Match Range

```sql
SELECT * FROM students WHERE age BETWEEN 18 AND 22;
```

---

## 10. IS NULL / IS NOT NULL

**Check for null:**

```sql
SELECT * FROM students WHERE email IS NULL;
```

**Check for not null:**

```sql
SELECT * FROM students WHERE email IS NOT NULL;
```

---

## 11. DISTINCT — Unique Values

```sql
SELECT DISTINCT course FROM students;
```

---

## 12. AS (Alias) — Rename Columns

```sql
SELECT name AS student_name, age AS student_age FROM students;
```

---

## 13. JOIN — Combine Tables

```sql
SELECT students.name, courses.course_name
FROM students
JOIN enrollments ON students.student_id = enrollments.student_id
JOIN courses ON courses.course_id = enrollments.course_id;
```

---

## 14. GROUP BY — Group Results
*Used to group rows that have the same values into summary rows. Often used with aggregate functions.*
```sql
SELECT course, COUNT(*) FROM students GROUP BY course;
```
---

## 15. HAVING — Filter Grouped Data
*Used to filter records after GROUP BY is applied. WHERE cannot be used here.*
```sql
SELECT course, COUNT(*)
FROM students
GROUP BY course
HAVING COUNT(*) > 1;
```
```sql
SELECT department, count(*) as number_of_records FROM `testDB`.`employees` GROUP BY department HAVING number_of_records >= 2 order by number_of_records ASC
```
---

## 16. Aggregate Functions

| Function | Description   | Example                         |
| -------- | ------------- | ------------------------------- |
| COUNT()  | Count rows    | SELECT COUNT(\*) FROM students; |
| SUM()    | Add values    | SELECT SUM(marks) FROM marks;   |
| AVG()    | Average value | SELECT AVG(age) FROM students;  |
| MAX()    | Highest value | SELECT MAX(age) FROM students;  |
| MIN()    | Lowest value  | SELECT MIN(age) FROM students;  |

---

## 17. Final Example — Combined Query

```sql
SELECT name
FROM students
WHERE age > 18 AND gender = 'Female'
ORDER BY name ASC
LIMIT 3;
```
---
##Join##
*A JOIN in SQL is used to combine rows from two or more tables based on a related column between them (usually a foreign key).*

**Types of JOINs in MySQL**
| JOIN Type         | Description                                                                                                     |
| ----------------- | --------------------------------------------------------------------------------------------------------------- |
| `INNER JOIN`      | Only returns rows with matching values in both tables.                                                          |
| `LEFT JOIN`       | Returns all rows from the left table, and matched rows from the right.                                          |
| `RIGHT JOIN`      | Returns all rows from the right table, and matched rows from the left.                                          |
| `FULL OUTER JOIN` | Returns all rows when there is a match in one of the tables. (Not supported directly in MySQL — needs `UNION`). |
| `SELF JOIN`       | Join a table with itself.                                                                                       |
| `CROSS JOIN`      | Returns Cartesian product (all combinations).                                                                   |

**1. INNER JOIN**
- Returns rows where there is a match in both tables



# Insert Qery # 
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);

# INSERT INTO Example
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');

# SQL DELETE
DELETE FROM table_name WHERE condition;
Example
DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';
# DROP TABLE
 DROP TABLE table_name;
** Example** : 
DROP TABLE Shippers;
