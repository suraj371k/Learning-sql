### **SQL Aggregate Functions**

An aggregate function is a function that performs a calculation on a set of values, and returns a single value.

### Group By

The `GROUP BY` clause splits the result-set into groups of values and the aggregate function can be used to return a single value for each group.

The most commonly used SQL aggregate functions are:

- `MIN()` - returns the smallest value within the selected column
- `MAX()` - returns the largest value within the selected column
- `COUNT()` - returns the number of rows in a set
- `SUM()` - returns the total sum of a numerical column
- `AVG()` - returns the average value of a numerical column

Aggregate functions ignore null values (except for `COUNT(*)`).

```sql
SELECT MIN(column_name)
FROM table_name
WHERE condition;

```

```sql
SELECT MIN(Price)
FROM Products;
```

```sql
SELECT MAX(Price)
FROM Products;
```

# Count

```sql
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
```

### Sum

```sql
SELECT SUM(column_name)
FROM table_name
WHERE condition;

```

### **SUM() With an Expression**

The parameter inside the `SUM()` function can also be an expression.

```sql
SELECT SUM(Quantity * 10)
FROM OrderDetails;
```

### AVG

The `AVG()` function returns the average value of a numeric column.

```sql
SELECT AVG(column_name)
FROM table_name
WHERE condition;

```

### Like Operator

The `LIKE` operator is used in a `WHERE` clause to search for a specified pattern in a column.

There are two wildcards often used in conjunction with the `LIKE` operator:

- The percent sign `%` represents zero, one, or multiple characters
- The underscore sign `_` represents one, single character

```sql
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```

### SQL Wildcard Characters

A wildcard character is used to substitute one or more characters in a string.

### Wildcard Characters

| Symbol | Description |
| --- | --- |
| % | Represents zero or more characters |
| _ | Represents a single character |
| [] | Represents any single character within the brackets * |
| ^ | Represents any character not in the brackets * |
| - | Represents any single character within the specified range * |
| {} | Represents any escaped character ** |

Note: Supported only oracle database not mysql or postgres

### The SQL IN Operator

The `IN` operator allows you to specify multiple values in a `WHERE` clause.

The `IN` operator is a shorthand for multiple `OR` conditions.

```sql
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);

```

### The SQL BETWEEN Operator

The `BETWEEN` operator selects values within a given range. The values can be numbers, text, or dates.

The `BETWEEN` operator is inclusive: begin and end values are included.