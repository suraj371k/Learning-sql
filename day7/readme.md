### CREATE DATABASE

The `CREATE DATABASE` statement is used to create a new SQL database.

```sql
CREATE DATABASE databasename;
```

### DROP DATABASE

The `DROP DATABASE` statement is used to drop an existing SQL database.

```sql
DROP DATABASE databasename;
```

### BACKUP DATABASE

The `BACKUP DATABASE` statement is used in SQL Server to create a full back up of an existing SQL database.

```sql
BACKUP DATABASE databasename
TO DISK = 'filepath';
```

### **BACKUP WITH DIFFERENTIAL Statement**

A differential back up only backs up the parts of the database that have changed since the last full database backup.

```sql
BACKUP DATABASE databasename
TO DISK = 'filepath'
WITH DIFFERENTIAL;
```

### CREATE TABLE

The `CREATE TABLE` statement is used to create a new table in a database.

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
```

### **Create Table Using Another Table**

```sql
CREATE TABLE new_table_name AS
    SELECT column1, column2,...
    FROM existing_table_name
    WHERE ....;
```

### **DROP TABLE**

The `DROP TABLE` statement is used to drop an existing table in a database.

```sql
DROP TABLE table_name;
```

### TRUNCATE TABLE

The `TRUNCATE TABLE` statement is used to delete the data inside a table, but not the table itself.

```sql
TRUNCATE TABLE table_name;
```

### **ALTER TABLE Statement**

The `ALTER TABLE` statement is used to add, delete, or modify columns in an existing table.

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

### **ALTER TABLE - DROP COLUMN**

To delete a column in a table, use the following syntax 

```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

### **ALTER TABLE - RENAME COLUMN**

```sql
ALTER TABLE table_name
RENAME COLUMN old_name to new_name;
```

### TO MODIFY DATATYPES

```sql
ALTER TABLE table_name
ALTER COLUMN column_name datatype;
```

### SQL constraints

SQL constraints are used to specify rules for data in a table.

The following constraints are commonly used in SQL:

- [`NOT NULL`](https://www.w3schools.com/sql/sql_notnull.asp) - Ensures that a column cannot have a NULL value
- [`UNIQUE`](https://www.w3schools.com/sql/sql_unique.asp) - Ensures that all values in a column are different
- [`PRIMARY KEY`](https://www.w3schools.com/sql/sql_primarykey.asp) - A combination of a `NOT NULL` and `UNIQUE`. Uniquely identifies each row in a table
- [`FOREIGN KEY`](https://www.w3schools.com/sql/sql_foreignkey.asp) - Prevents actions that would destroy links between tables
- [`CHECK`](https://www.w3schools.com/sql/sql_check.asp) - Ensures that the values in a column satisfies a specific condition
- [`DEFAULT`](https://www.w3schools.com/sql/sql_default.asp) - Sets a default value for a column if no value is specified
- [`CREATE INDEX`](https://www.w3schools.com/sql/sql_create_index.asp) - Used to create and retrieve data from the database very quickly

### FOREIGN KEY

A `FOREIGN KEY` is a field (or collection of fields) in one table, that refers to the [`PRIMARY KEY`](https://www.w3schools.com/sql/sql_primarykey.asp) in another table.

```sql
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
```

```sql
ALTER TABLE Orders
ADD FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);
```

### **DROP a FOREIGN KEY Constraint**

```sql
ALTER TABLE Orders
DROP FOREIGN KEY FK_PersonOrder;
```

### CHECK

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CHECK (Age>=18)
);
```

### **DEFAULT Constraint**

The `DEFAULT` constraint is used to set a default value for a column.

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255) DEFAULT 'Sandnes'
);
```

### SQL CREATE INDEX Statement

The `CREATE INDEX` statement is used to create indexes in tables.

Indexes are used to retrieve data from the database more quickly than otherwise. The users cannot see the indexes, they are just used to speed up searches/queries.

```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

### AUTO INCREMENT Field

Auto-increment allows a unique number to be generated automatically when a new record is inserted into a table.

Often this is the primary key field that we would like to be created automatically every time a new record is inserted.

```sql
CREATE TABLE Persons (
    Personid int NOT NULL AUTO_INCREMENT,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (Personid)
);
```

# SQL Date Data Types

**MySQL** comes with the following data types for storing a date or a date/time value in the database:

- `DATE` - format YYYY-MM-DD
- `DATETIME` - format: YYYY-MM-DD HH:MI:SS
- `TIMESTAMP` - format: YYYY-MM-DD HH:MI:SS
- `YEAR` - format YYYY or YY

# SQL Injection

SQL injection is a code injection technique that might destroy your database.

SQL injection is one of the most common web hacking techniques.

SQL injection is the placement of malicious code in SQL statements, via web page input.

# SQL in Web Pages

SQL injection usually occurs when you ask a user for input, like their username/userid, and instead of a name/id, the user gives you an SQL statement that you will **unknowingly** run on your database.