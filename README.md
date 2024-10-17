# SQL-JOINS
Understanding SQL Joins: LEFT, RIGHT, INNER, CROSS, and SELF Joins 

QL Joins are a crucial part of database management, helping you retrieve related data from different tables in a structured way. <br> Allows you to combine data from multiple tables based on related columns.<br>
Let’s dive into the types of joins—LEFT, RIGHT, INNER, CROSS, and SELF—and understand their use cases in a concise, easy-to-follow format.


## What Are SQL Joins?
SQL joins combine data from two or more tables in a database by specifying a condition that defines how the tables are related.<br>
Helps retrieve meaningful data by linking tables through common fields like PRIMARY and FOREIGN KEYS.<br> <br>

Let’s walk through each type of join.

## Types of SQL Joins:

## 1. INNER JOIN
**What it does:** Return only the rows where there is a match in both tbales.<br>
**Use Case:** When you want to fetch only matching data across tbales.<br>
**Example:** Retrieving orders that have valid customer IDs in both the ORDERS and CUSTOMERS tables.

### *Syntax:*
```
SELECT columns
FROM table1
INNER JOIN table2 ON table1.column = table2.column;
```

## 2. LEFT JOIN (LEFT OUTER JOIN)
**What it does:** Return all rows from the left table and the matched rows from the right table. If no match, NULL is returned for the right table.<br>
**Use Case:** When you want all records from one table, even if there is no match in the other.<br>
**Example:** FEtching all cusomters, including those wothout orders.

### *Syntax:*
```
SELECT columns
FROM table1
LEFT JOIN table2 ON table1.column = table2.column;
```

## 3. RIGHT JOIN (RIGHT OUTER JOIN)
**What it does:** Returns all rows from the right table and the matched rows from the left table. If no match, NULL is returned for the left table.<br>
**Use Case:** When you need all records from right table, regardless of matches in the left.<br>
**Example:** Listing all orders, even if some customers are missing.

## *Syntax:*
```
SELECT columns
FROM table1
RIGHT JOIN table2 ON table1.column = table2.column;
```

## 4. CROSS JOIN
**What it does:** Returns the CArtesian product of both tables (i.e., all possible combinations)<br>
**Use Case:** When every combination of data is needed from two tbales.<br>
**Example:** Pairing every customer with every product for promotional offers.

## *Syntax:*
```
SELECT COLUMNS 
FROM table1
CROSS JOIN table2;
```

## *5. SELF JOIN*
**What it does:** Joins a table with itself. <br>
**Use Case:** To compare rows within same table. <br>
**Example:** Finding employees who report to the same manager.

## *Syntax:*
```
SELECT a.columns, b.columns
FROM table a, table b
WHERE a.column = b.column;
```

## Quick Summary:
* INNER JOIN: Fetches only matching rows from both tables.
+ LEFT JOIN: All rows from the left table and matching rows from the right.
- RIGHT JOIN: All rows from the right table and matching rows from the left.
+ CROSS JOIN: Every possible combination of rows between two tables.
* SELF JOIN: A table joined with itself for internal comparisons.

## WHEN TO USE??

* INNER JOIN: When you need related data from both tables.
+ LEFT JOIN: When one table has all the data you need, but you also want to include available matches from the other table.
- RIGHT JOIN: Same as LEFT JOIN but in reverse.
+ CROSS JOIN: For all possible combinations of rows.
* SELF JOIN: To compare rows within the same table.

