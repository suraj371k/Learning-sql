### Order by:

the ORDER by keyword is used to sort the result in ascending or descending order.

by default it sorts in ascending order

- Sorts in ascending order

```sql
SELECT * FROM Products
ORDER BY Price;

```

- Sorts in descending order

```sql
SELECT * FROM Products
ORDER BY Price DESC
```

- order by several column

```sql
SELECT * FROM Customers
ORDER BY Country, CustomerName;
```

- Using both ascending and descending order

```sql
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;

```

### **AND Operator**

The `WHERE` clause can contain one or many `AND` operators.

The `AND` operator is used to filter records based on more than one condition, like if you want to return all customers from Spain that starts with the letter 'G'

- Select all customers from Spain that starts with the letter 'G':

```sql
Select all customers from Spain that starts with the letter 'G':

```

### AND VS OR

The `AND` operator displays a record if *all* the conditions are TRUE.

The `OR` operator displays a record if *any* of the conditions are TRUE.

### The SQL OR Operator

The `WHERE` clause can contain one or more `OR` operators.

The `OR` operator is used to filter records based on more than one condition, like if you want to return all customers from Germany but also those from Spain:

- Select all customers from Germany or Spain:

```sql
SELECT *
FROM Customers
WHERE Country = 'Germany' OR Country = 'Spain';
```

### The NOT Operator

The `NOT` operator is used in combination with other operators to give the opposite result, also called the negative result.

- Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;

```

Example:

```sql
SELECT * FROM Customers
WHERE NOT Country = 'Spain';
```

Select customers that are not from Paris or London:

```sql
SELECT * FROM CustomersWHERE City NOT IN ('Paris', 'London');
```

### INSERT INTO

the INSERT INTO statment is used to insert new records in a table.

It is possible to write the `INSERT INTO` statement in two ways:

1. Specify both the column names and the values to be inserted:

```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

1. If you are adding values for all the columns of the table , you do not need to specify the column names in SQL query.

```sql
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```