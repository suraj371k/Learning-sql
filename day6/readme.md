### GROUP BY

**`GROUP BY` in SQL** is used to **group rows that have the same values in one or more columns**, usually so you can apply **aggregate functions** like `COUNT`, `SUM`, `AVG`, `MAX`, or `MIN`.

```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```

### HAVING CLAUSE

The `HAVING` clause was added to SQL because the `WHERE` keyword cannot be used with aggregate functions.

```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```

### EXIST OPERATOR

The `EXISTS` operator is used to test for the existence of any record in a subquery.

The `EXISTS` operator returns TRUE if the subquery returns one or more records.

```sql
SELECT column_name(s)
FROM table_name
WHERE EXISTS
(SELECT column_name FROM table_name WHERE condition);
```

### ANY

**`ANY` in SQL** is used to compare a value with **a set of values returned by a subquery**.

The condition is true if the comparison is true for **at least one** value in the subquery.

```sql
SELECT column_name(s)
FROM table_name
WHERE column_name operator ANY
  (SELECT column_name
  FROM table_name
  WHERE condition);
```

### SELECT INTO

The `SELECT INTO` statement copies data from one table into a new table.

### copy all columns

```sql
SELECT *
INTO newtable [IN externaldb]
FROM oldtable
WHERE condition;
```

### copy only some columns into new table

```sql
SELECT column1, column2, column3, ...
INTO newtable [IN externaldb]
FROM oldtable
WHERE condition;
```

### **SQL INSERT INTO SELECT Statement**

The `INSERT INTO SELECT` statement copies data from one table and inserts it into another table.

The `INSERT INTO SELECT` statement requires that the data types in source and target tables match.

```sql
INSERT INTO table2
SELECT * FROM table1
WHERE condition;
```

```sql
Copy only some columns from one table into another table:

INSERT INTO table2 (column1, column2, column3, ...)
SELECT column1, column2, column3, ...
FROM table1
WHERE condition;
```

### SQL CASE EXPRESSION

The `CASE` expression goes through conditions and returns a value when the first condition is met (like an if-then-else statement). So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the `ELSE` clause.

```sql
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```

# Stored Procedure?

A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over again.

So if you have an SQL query that you write over and over again, save it as a stored procedure, and then just call it to execute it.

# Stored Procedure Syntax

```sql
CREATE PROCEDURE procedure_name
AS
sql_statement
GO;
```

**Execute a Stored Procedure**

```sql
EXEC procedure_name;
```

### SQL COMMENTS

Comments are used to explain sections of SQL statements, or to prevent execution of SQL statements.

### **Single Line Comments**

Single line comments start with `--`.

Any text between -- and the end of the line will be ignored (will not be executed).

```sql
-- Select all:
SELECT * FROM Customers;
```

### **Multi-line Comments**

Multi-line comments start with `/*` and end with `*/`.

```sql
/*Select all the columns
of all the records
in the Customers table:*/
SELECT * FROM Customers;
```

# SQL Arithmetic Operators

| Operator | Description |
| --- | --- |
| + | Add |
| - | Subtract |
| * | Multiply |
| / | Divide |
| % | Modulo |

---

# SQL Bitwise Operators

| Operator | Description |
| --- | --- |
| & | Bitwise AND |
| | | Bitwise OR |
| ^ | Bitwise exclusive OR |

---

# SQL Comparison Operators

| Operator | Description |
| --- | --- |
| = | Equal to |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal to |
| <= | Less than or equal to |
| <> | Not equal to |

---

# SQL Compound Operators

| Operator | Description |
| --- | --- |
| += | Add equals |
| -= | Subtract equals |
| *= | Multiply equals |
| /= | Divide equals |
| %= | Modulo equals |
| &= | Bitwise AND equals |
| ^= | Bitwise exclusive equals |
| |*= | Bitwise OR equals |

---

# SQL Logical Operators

| Operator | Description |
| --- | --- |
| ALL | TRUE if all of the subquery values meet the condition |
| AND | TRUE if all the conditions separated by AND is TRUE |
| ANY | TRUE if any of the subquery values meet the condition |
| BETWEEN | TRUE if the operand is within the range of comparisons |
| EXISTS | TRUE if the subquery returns one or more records |
| IN | TRUE if the operand is equal to one of a list of expressions |
| LIKE | TRUE if the operand matches a pattern |
| NOT | Displays a record if the condition(s) is NOT TRUE |
| OR | TRUE if any of the conditions separated by OR is TRUE |
| SOME | TRUE if any of the subquery values meet the condition |