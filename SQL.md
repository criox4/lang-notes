# SQL Notes

SQL commands can be categorized  into 5 catogoories: 
1. DDL - Data Definition Language
2. DQL - Data Query Language
3. DML - Data Manipulation Language
4. DCL - Data Control Language
5. TCL - Transaction Control Language

## DDL - Data Definition Language 
1. CREATE
2. DROP 
3. ALTER 
4. TRUNCATE

CREATE TABLE - Create A TABLE

```sql
CREATE TABLE <Table Name>(
        ID <DATA TYPE> <PRIMARY KEY>,
        COL1 <DATA TYPE> ,......
    );
```

Example: 

```sql
CREATE TABLE employees(
    emp_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    desg VARCHAR(50)
);
```


DROP TABLE - Drop the table ( including all the rows and columns ) i.e. delete the whole table

```sql
DROP TABLE <Table Name>
```

TRUNCATE - Delete all the data from the table i.e. all the rows from the table. 

```sql
TRUNCATE TABLE <Table NAME>
```
Example : 
```sql
TRUNCATE TABLE employees;
```

ALTER  - Changes the Structure of table  i.e. add, delete , modify column

It has 3 commands  : 

ADD - add a column 
```sql
ALTER TABLE <table name> 
ADD COLUMN < column name > <column data type>
```


DROP - Delete a column
```sql
ALTER TABLE <table name> 
DROP COLUMN < column name >
```

Modify - Change the Data Type
```sql
ALTER TABLE <table name> 
MODIFY  <column name> <column data type>
```
RENAME TO / RENAME COLUMN - Rename the Table Name/ Rename the Column ( ONLY FOR MYSQL )
```sql
ALTER TABLE table_name
RENAME COLUMN old_name TO new_name;
```

```sql
ALTER TABLE table_name
RENAME TO new_table_name;
```
EXAMPLE:
```sql
ALTER TABLE employees ADD COLUMN phone VARCHAR(10);
ALTER TABLE employees DROP COLUMN phone ;
ALTER TABLE employees RENAME COLUMN desg TO designation;
```


