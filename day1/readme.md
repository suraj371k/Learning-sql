# SQL Learning – Day 1

## What is a Spreadsheet?

* A spreadsheet is a file that consists of cells arranged in rows and columns.
* It helps to arrange, calculate, analyze, and sort data efficiently.

---

## What is a Database?

* A database is an organized collection of data.
* It is arranged for ease and speed of searching, storing, and retrieving information.

---

## What is SQL?

**SQL (Structured Query Language)** is used to manage and manipulate data stored in relational databases such as:

* MySQL
* PostgreSQL
* Oracle
* SQL Server

---

## What are Tables, Rows, and Columns?

### Table

* A table is where data is stored in a database.
* It is similar to a sheet in a spreadsheet.

**Example:** `Student` table

---

### How to Create a Table

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype
);
```

---

### Rows (Records)

* A row represents one complete entry in a table.
* Each row contains related information.
* A row is also called a **record**.

**Example (one row):**
A single student’s information

```text
(1, "Rahul", 20, "Computer Science")
```

---

### Columns (Fields)

* A column represents one type of data in a table.
* Each column has a **name** and a **data type**.
* The same kind of data is stored in a column for all rows.

**Example columns:**

* `student_id`
* `name`
* `age`
* `department`

---

## SELECT Statement

* The `SELECT` statement is used to retrieve data from a database.

```sql
SELECT CustomerName, City
FROM Customers;
```

---

## SELECT DISTINCT Statement

* The `SELECT DISTINCT` statement is used to return only unique values.

**Example: Count distinct countries**

```sql
SELECT COUNT(DISTINCT Country)
FROM Customers;
```

---

## WHERE Clause

* The `WHERE` clause is used to filter records.
* It extracts only those records that fulfill a specified condition.

**Note:**
The `WHERE` clause can be used with `SELECT`, `UPDATE`, `DELETE`, etc.

---

### Operators Used in WHERE Clause

* Equal to (`=`)
* Greater than (`>`)
* Less than (`<`)
* Greater than or equal to (`>=`)
* Less than or equal to (`<=`)
* `BETWEEN` – selects values within a range
* `LIKE` – searches for a pattern
* `IN` – specifies multiple possible values


## Day 1 Practice Questions:

- Retrieve all columns from a "customers" table
- Select only the "name" and "email" columns from a "users" table
- Find all products where the price is greater than 50
- Display all employees whose department is 'Sales'
- List all orders where the quantity is exactly 10

