
### Null Value

A field with null value is a field with no value.

**Note:** A null value is different from zero value or a field that contains space.

A field with a NULL value is one that has been left blank during record creation!

### How to test a null value

To test a null value we can use IS NULL or IS NOT NULL operators

```sql
SELECT column_names
FROM table_name
WHERE column_name IS NULL;
```

### UPDATE statement:

The update statement is used to modify the existing record from the table.

**Note**: Do not forget to add where clause while updating the values if you not specify where clause it will update all the value in the table.

```sql
UPDATE Customers
SET ContactName = 'Suraj', City= 'Lucknow'
WHERE CustomerID = 1;
```

### DELETE Statement

The DELETE Statement is used to delete the existing record in a table.

```sql
DELETE FROM Customers WHERE CustomerName='Suraj Kushwaha';
```

### To delete all records

```sql
DELETE FROM table_name;

```

### **Delete a Table**

```sql
DROP TABLE Customers;
```

### Limit

The is used to specify the number of records to return.

```sql
SELECT * FROM Customers
LIMIT 3;
```