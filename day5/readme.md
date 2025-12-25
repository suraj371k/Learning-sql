### SQL JOIN

A `JOIN` clause is used to combine rows from two or more tables, based on a related column between them.

### **Different Types of SQL JOINs**

- `(INNER) JOIN`
- `LEFT (OUTER) JOIN`
- `RIGHT (OUTER) JOIN`
- `FULL (OUTER) JOIN`

### INNER JOIN

The `INNER JOIN` keyword selects records that have matching values in both tables.

```sql
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;

```

![image.png](attachment:9e6176f1-69ae-434c-816a-a27e8c20cdec:image.png)

**Note:** `INNER` is the default join type for `JOIN`, so when you write `JOIN` the parser actually writes `INNER JOIN`.

### LEFT JOIN

The `LEFT JOIN` keyword returns all records from the left table (table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.

```sql
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

![image.png](attachment:902a5458-c673-4f7d-9642-88a39cffa75d:image.png)

### RIGHT JOIN

The `RIGHT JOIN` keyword returns all records from the right table (table2), and the matching records from the left table (table1). The result is 0 records from the left side, if there is no match.

```sql
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```

![image.png](attachment:5e0b263b-dc11-4647-9a8c-675649797e43:image.png)

**Note:** The `RIGHT JOIN` keyword returns all records from the right table , even if there are no matches in the left table .

### FULL JOIN

The `FULL OUTER JOIN` keyword returns all records when there is a match in left (table1) or right (table2) table records.

```sql
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;
```

![image.png](attachment:5d0d222d-de7e-4b21-9766-d285fa5004d0:image.png)

### SELF JOIN

A self join is a regular join, but the table is joined with itself.

```sql
SELECT column_name(s)
FROM table1 T1, table1 T2
WHERE condition;
```

### UNION OPERATOR

The `UNION` operator is used to combine the result-set of two or more `SELECT` statements.

The `UNION` operator automatically removes duplicate rows from the result set.

### Requirements for `UNION`:

- Every `SELECT` statement within `UNION` must have the same number of columns
- The columns must also have similar data types
- The columns in every `SELECT` statement must also be in the same order

```sql
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```

### UNION ALL

The `UNION ALL` operator is used to combine the result-set of two or more `SELECT` statements.

The `UNION ALL` operator includes all rows from each statement, including any duplicates.

### Requirements for `UNION ALL`:

- Every `SELECT` statement within `UNION ALL` must have the same number of columns
- The columns must also have similar data types
- The columns in every `SELECT` statement must also be in the same order

```sql
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
```