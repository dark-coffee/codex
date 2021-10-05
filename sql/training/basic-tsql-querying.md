# Basics of T-SQL Querying

![Slide Cover](https://shadow.coffee/bucket/sql-server/basics.png)

## SQL Overview

### SQL

- SQL stands for “Structured English Query Language”.
- Pronounced “ESS-KEW-EL” or colloquially “Sequel”.
- Structured Query Language is used to interact, and communicate with databases.
  - SQL is easily “human-readable” compared to other popular programming languages.
  - Essentially, it’s mostly plain English.
- SQL is the “open source” version; T-SQL (Transact-SQL) is the Microsoft variant. (T-SQL was created by Microsoft and Sybase).
  - Contains most of the open source functions but is expanded greatly.

### SQL Server

- In a nutshell, SQL Server is two things:
  1. A physical or virtual server used to run and operate an instance of SQL Server.
  2. The software SQL Server, is the instance used to parse and perform operations upon a set of databases.
- It is possible to run more than one instance of SQL Server on a physical/virtual SQL Server.
  - For SME's, this is not recommended due to performance reasons.
  - Additionally you can run it along side other programs, again, this is not recommended due to performance impacts.

---

## Databases

- A database is a structured set of Data held on a computer that can be accessed in numerous ways.
- In terms of SQL Server, this is a collection of views, schemas, logins, tables, queries and other objects.
- In SQL Server, you can access nearly everything using T-SQL.

- Most databases are relational.
- Relational databases are made by using a set of tables containing data.
- Data is mostly unique – to prevent you from storing the same data twice.
- The data is linked together using a relationship.
- Relational databases have a performance advantage, in terms of both size, and speed.

---

## Tables

### Overview

- A location within a database to store information.
- Properties:
  - Columns (vertical)
  - Rows (horizontal)
  - Cells (the intersection of those two)
- A table stores a specific set of data in a specific way
- An easy way to think of a table, is to think of an Excel spreadsheet

### Example Table

| Patient Ref | Title | Forename | MiddleInitial | Surname | DoB        | NationalCode | HomePhone   | MobileNumber |
| ----------- | ----- | -------- | :-----------: | ------- | ---------- | ------------ | ----------- | ------------ |
| 00001       | Mr    | Daniel   |       J       | Stock   | 1990-07-16 | 111 111 1111 | 01233722707 | 07951505052  |
| 00002       | Mr    | Chris    |       P       | Duck    | 1989-02-28 | 222 222 2222 | 01233722700 | 07942432953  |
| 00003       | Miss  | Laura    |       F       | Hyde    | 1975-05-07 | 333 333 3333 | 01622016220 | 07036339498  |
| 00004       | Dr    | Not      |       A       | Doctor  | 2001-05-12 | 444 444 4444 | 01234567890 | 07808207889  |
| 00005       | Mrs   | Amy      |       W       | Hughes  | 1996-01-23 | 555 555 5555 | 01242628492 | 07980157371  |
| 00006       | Mrs   | Jasmine  |       Y       | Sanders | 1994-10-15 | 666 666 6666 | 01634199482 | 07700220441  |
| 00007       | Mr    | Jason    |       D       | Frank   | 1979-03-16 | 777 777 7777 | 01458293725 | 07823760012  |

### Primary & Foreign Keys

- If multiple tables are being used, then they need to be linked (relationship)
- There are two ways of linking tables:
  - Primary Keys
  - Foreign Keys
- Primary Key:
  - Provides a unique reference for each record
  - Each individual table requires one
  - It acts as a reference point allowing tables to be interlinked
  - Can be comprised of a combination of columns (composite primary key)
- Foreign Key:
  - A field or collection of keys within a table, that uniquely identifies a row in a different table
  - Essentially, it creates a relationship between tables

#### Primary & Foreign Keys - Example Table

In this example, `ID` is the primary key of the **Staff** table (left), with `Staff No.` being the primary key of the **Staff Details** table (right), and foreign key of the **Staff** table.

| ID  | Title | Forename | MiddleInitial | Surname | Staff No. | _break_ | Staff No. | DoB        | NationalCode | HomePhone   | MobileNumber |
| --- | ----- | -------- | :-----------: | ------- | --------- | ------- | --------- | ---------- | ------------ | ----------- | ------------ |
| 1   | Mr    | Daniel   |       J       | Stock   | 784       |         | 784       | 1990-07-16 | 111 111 1111 | 01233722707 | 07951505052  |
| 2   | Mr    | Chris    |       P       | Duck    | 321       |         | 321       | 1989-02-28 | 222 222 2222 | 01233722700 | 07942432953  |
| 3   | Miss  | Laura    |       F       | Hyde    | 141       |         | 141       | 1975-05-07 | 333 333 3333 | 01622016220 | 07036339498  |
| 4   | Dr    | Not      |       A       | Doctor  | 123       |         | 123       | 2001-05-12 | 444 444 4444 | 01234567890 | 07808207889  |
| 5   | Mrs   | Amy      |       W       | Hughes  | 50        |         | 50        | 1996-01-23 | 555 555 5555 | 01242628492 | 07980157371  |
| 6   | Mrs   | Jasmine  |       Y       | Sanders | 146       |         | 146       | 1994-10-15 | 666 666 6666 | 01634199482 | 07700220441  |
| 7   | Mr    | Jason    |       D       | Frank   | 456       |         | 456       | 1979-03-16 | 777 777 7777 | 01458293725 | 07823760012  |

### Constraints

- **SQL** constraints are used to specify rules for the data in a table.
- **NOT NULL** – Indicates a column that cannot store **NULL** value.
- **UNIQUE** - Ensures that each row for a column must have a unique value.
- **PRIMARY KEY** - A combination of a **NOT NULL** and **UNIQUE**. Ensures that a column (or combination of two or more columns) have a unique identity which helps to find a particular record in a table more easily and quickly.
- **FOREIGN KEY** - Ensure the referential integrity of the data in one table to match values in another table.
- **CHECK** - Ensures that the value in a column meets a specific condition.
- **DEFAULT** - Specifies a default value when specified none for this column.

### Common Datatypes

Columns within a table specify a type of data that is contained in each cell of that column.

| Datatype      | Description                                                                                                      |
| ------------- | ---------------------------------------------------------------------------------------------------------------- |
| VARCHAR(n)    | A string of characters. n is the maximum length of the field – VARCHAR(50).                                      |
| INTEGER /INT  | Integer number. No decimal places.                                                                               |
| DECIMAL (p,s) | Number with decimal places. p is precision (total length of number). s is scale (of p, how many decimal places). |
| DATE          | I’d be stating the obvious.                                                                                      |
| TIME          | “.                                                                                                               |
| DATETIME      | “. But has many different formats.                                                                               |
| SMALLMONEY    | Monetary value between -214,748.3648 and 214,748.3647                                                            |
| MONEY         | (SMALLMONEY but bigger?) Monetary value between -922,337,203,685,477.5808 and 922,337,203,685,477.5807           |

---

## Queries & Clauses

### SELECT

- A `SELECT` statement is used to select data from a database.
- The result is stored in a table referred to as the “result set”.
- It is good practice to type your clauses in uppercase.

```sql
SELECT
    PatientRef,
    Forename,
    Surname,
    DoB
  FROM patient;
```

- However, as an alternative to specifying each and every column, we can use an asterisk to bring back all of the columns.

```sql
SELECT *
  FROM patient;
```

- A `SELECT` statement must be made up of the following components:
  - The `SELECT` clause.
  - The column names you wish to select, or a wildcard.
  - The `FROM` clause to choose the location that you are selecting from. (If the `FROM` clause is not used, or does not have a specified table, the query will error.)

### DISTINCT

The `DISTINCT` clause is used to select data without duplicate values.
This should only be used when you wish to select `DISTINCT` data from one column.

```sql
SELECT DISTINCT Surname
  FROM patient;
```

### WHERE

- In order to select records from a table that only meet certain criteria – we can use the `WHERE` operator.
- `WHERE` will limit or filter the results of a query.
- The `WHERE` statement will always come after the `FROM` operator.

```sql
  SELECT [column]
    FROM [table]
   WHERE [criteria];

```

There are several operators that will change the functionality of the `WHERE` clause:

| Operator | Meaning                  | Example                                          |
| :------: | ------------------------ | ------------------------------------------------ |
|    =     | Equals                   | `WHERE x = y`                                    |
|    <     | Less than                | `WHERE x < y`                                    |
|    >     | Greater than             | `WHERE x > y`                                    |
|    <=    | Less than or equal to    | `WHERE x <= y`                                   |
|    >=    | Greater than or equal to | `WHERE x >= y`                                   |
|    !=    | Not equal to             | `WHERE x != y`                                   |
|    <>    | Not equal to             | `WHERE x <> y`                                   |
| BETWEEN  | Between x and y          | `WHERE Date BETWEEN ‘01 Jan 20’ AND ‘31 JAN 20’` |

#### Further operators

- `IN` - this can be used to specify one or more values to match: `WHERE surname IN (‘Smith’, ‘Stock’, ‘Jones’);`
- `VARCHAR` – if using `WHERE` to match a varchar field (essentially free text), you will need to put your text to match in single quotes. By default, SSMS will turn these text inputs red: `WHERE surname = Smith;`

#### WHERE - Example Queries

**Query 1**: This query will return all columns from the patient table, where the surname is Smith. i.e. every patient who’s surname is Smith.

```sql
SELECT *
  FROM patient
 WHERE surname = ‘Smith’;
```

**Query 2**: This query will return all columns from the case table, with a case number greater than or equal to 1337. Single quotes are not required for integer fields.

```sql
SELECT *
  FROM case
 WHERE caseno >= 1337;
```

### Logical Operators

- To further customise the results of our chosen query, we can combine what is essentially multiple `WHERE` clauses with logical operators:
  - `AND` can be used when 2 (or more) `WHERE`s need to be met at the same time.
  - `OR` can be used when any 1 of 2 (or more) `WHERE`s can be met.
- You can also combine these in many different and exciting ways to ensure that you only return the data you want.

#### Logical Operators - Example Queries

**Query 1**: This query will return the forename, surname and DoB for all patients who’s name is **John Smith**.

```sql
SELECT
    forename,
    surname,
    DoB
  FROM patient
 WHERE forename = ‘John’
   AND surname = ‘Smith’;
```

**Query 2**: This query will return the forename, surname and DOB for all patients named **Dan** or **Daniel**.

```sql
SELECT
    forename,
    surname,
    DoB
  FROM patient
 WHERE forename = ‘Dan’
    OR forename = ‘Daniel’;
```

### TOP

To return only a certain number of records with a query, we can use the `TOP` operator to specify how many rows to return. `TOP` will return the first (x) records as specified.

```sql
SELECT TOP(25) *
  FROM patient
```

This query will return the first 25 patients from the patients table.

### ORDER BY

- By default, SQL decides how best to display the records returned. Usually this is an acceptable order for viewing the data.
- If you wish to override this order, you can specify the order by utilising the `ORDER BY` clause.

```sql
  SELECT *
    FROM [table]
ORDER BY [column] ASC/DESC;
```

- To specify ascending or descending, use `ASC` or `DESC` appropriately.
- If neither `ASC` or `DESC` are specified, SQL will assume `ASC`.

#### ORDER BY - Example Queries

**Query 1**: This query will select all columns from the log table, but only the top 200 rows, sorted by date descending (most recent first).

```sql
  SELECT TOP(200) *
    FROM log
ORDER BY Date DESC;
```

**Query 2**: This query will select all rows from the case table ordered by their case number, in an ascending fashion.

```sql
  SELECT *
    FROM case
ORDER BY caseno ASC;
```

### Date & Date Ranges

- When running a query with a `WHERE` clause, it is advisable to first filter by date (if possible!).
- In most cases, date is normally indexed. This will cause the results to be returned faster, and will use less resources on the database server.
- Filtering by date also reduces the quantity of records returned.

```sql
SELECT *
  FROM patient
 WHERE DoB > ‘1993-03-20’;
```

This query will return all columns all patients with a DoB greater than March 20th 1993.

### LIKE & Wildcards

- A wildcard refers to a character that can be used to substitute for zero or more unknown characters.
- Useful if you’re trying to find something, but you know only part of the value.
- You can use more than one wildcard together for an exciting combination!

| Symbol | Meaning                                                | Example                                            |
| :----: | ------------------------------------------------------ | -------------------------------------------------- |
|   %    | Matches 0 or more characters.                          | ‘Si%’ will find “Sign”, “Signal” etc               |
|   \_   | Matches 1 character.                                   | ‘Sig\_’ will find “Sigh”, “Sign” etc.              |
|  [ ]   | Matches any of the characters **within** the brackets. | ‘H\[ai]t’ will find “Hat”, “Hit” but not “Hot”.    |
|   ^    | Matches any of the characters **not** in the brackets. | ‘H\[^ai]t’ will find “Hot” but not “Hit” or “Hat”. |
|   -    | Matches a range of characters.                         | ‘H[a-c]t’ will find “Hat”, “Hbt”, “Hct”.           |

#### LIKE & Wildcards - Example Queries

**Query 1**: This query will return the forename and the surname for any patient whose surname begins with Smith. This would include results such as ‘Smith’, ‘Smithson’, ‘Smithenberry’ etc.

```sql
SELECT
    forename,
    surname
  FROM patient
 WHERE surname LIKE ‘Smith%’;
```

**Query 2**: If we substitute ‘Smith%’ for ‘%smith’ this would bring back patients with a surname that ends in smith. This would include results such as ‘Goldsmith’, ‘Blacksmith’ etc.

```sql
SELECT
    forename,
    surname
  FROM patient
 WHERE surname LIKE ‘%smith’;
```

---

## Joins & Unions

### Joins

- A JOIN allows you to select data from multiple tables using a link (Primary and Foreign Keys).
- There are four types of `JOIN`, each with a different function. `LEFT JOIN` and `RIGHT JOIN` can return `NULL`.

![Join Diagram](https://shadow.coffee/bucket/sql-server/basics-joins2.png)

- Standard SQL syntax applies, meaning you can apply other clauses (such as `WHERE`) when needed.

#### Joins - Example Joins

Example of an `INNER JOIN`. This combines columns from 1 or more tables, which can be saved as a table or used in result form.

```sql
    SELECT *
      FROM [case]
INNER JOIN [patient] ON [case].[patientref] = [patient].[patientref];
```

Example of a `LEFT JOIN`. This will return all rows from the left table, with the matching rows from the right table – provided there is a match. If there is no match, `NULL` will be returned for the right table.

```sql
   SELECT *
     FROM [case]
LEFT JOIN [patient] ON [case].[patientref] = [patient].[patientref];
```

When using a `JOIN`, if you wish to select a specific column, you will need to specify the table name as well.

```sql
    SELECT [table1].[columname],[table2].[columnname]
      FROM [table1]
INNER JOIN [table2] ON [table1].[columnname] = [table2].[columnname];
```

### Unions

![Union Diagram](https://shadow.coffee/bucket/sql-server/basics-unions2.png)

- A UNION will combine the results from multiple tables, removing any duplicate rows.
- Useful if you want to see all the data from multiple tables in one result set.
- Unions are resource intensive so should be avoided wherever possible.
- The columns in the tables must match exactly for a union to work (same number of columns, same datatypes).
- Joins are horizontal, but Unions are vertical.
- You can force display duplicate rows by using UNION ALL.

#### Unions - Example Union

```sql
SELECT
    country,
    region,
    Id
  FROM EU.Nationals 
UNION
SELECT
    country,
    region,
    Id
  FROM UK.Nationals;
```

| Country |    Region     |    Id     |
| :-----: | :-----------: | :-------: |
|   UK    | West Midlands | I5789178Z |
| Germany |    Hessen     | Y8917234X |
| France  |  Rhone-Alpes  | T9128370Q |
|   UK    |    Anglia     | I9328401P |

---

## Transactions

### Transactions - Overview

[Tom Scott - The Worst Typo I Ever Made](https://www.youtube.com/watch?v=X6NJkWbM1xk)

### Transactions - Usage

- In MSSQL, transactions are opened with `BEGIN TRAN`.
- To close a transaction and save the changes, type `COMMIT` or `COMMIT TRAN`.
- To close a transaction and discard the changes, type `ROLLBACK` or `ROLLBACK TRAN`.

- An open transaction (e.g. using `BEGIN TRAN` and then not following it with `COMMIT` or `ROLLBACK`) will lock the table(s) being operated upon and prevent all writing until the transaction is committed or rolled back.

  - Open transactions are to be avoided **at all costs**.

- When finished, if you are unsure if a transaction is still open, you can run `PRINT @@TRANCOUNT` – if the number is not 0, then there is an open transaction.

- If updating the database, you must **ALWAYS** use a transaction.

---

## Update

### Update - Overview

The UPDATE command updates fields in the database.

Unless you fully understand the UPDATE command and it’s consequences, do not use it.
If issuing an UPDATE command, you must use a transaction.
Partially to protect yourself, partially for data integrity.
Before issuing an UPDATE command, have someone sanity-check your work.

### Update - Example

Example of an UPDATE statement:

```sql
UPDATE [staff]
   SET Surname = 'Smith'
 WHERE Surname = 'Smit';
```

This will update the surname column in the staff table, where the surname is spelt incorrectly.

### Update - Components

UPDATE Statements are made up of several component parts:

1. The table you’re updating: `UPDATE [Staff]`
2. The column name, and the new value to set: `SET Surname = 'Smith'`
3. Criteria to determine which columns to change" `WHERE Surname = 'Smit'`

### Update - Process

It is good practice to run a SELECT statement before writing the UPDATE to ensure you know what will be changed

```sql
  SELECT *
    FROM [staff]
   WHERE Surname = 'Smit';
```

Perform the UPDATE inside a transaction

```sql
BEGIN TRAN
UPDATE [staff]
   SET Surname = 'Smith'
 WHERE Surname = 'Smit';
```

Check the change with another SELECT statement

```sql
  SELECT *
    FROM [staff]
   WHERE Surname = 'Smit';
```

If you are happy save your change, or undo

```sql
  COMMIT / ROLLBACK;
```

---

## Useful Stuff

### Commands & Tricks

- `COUNT()` - returns the number of rows that matches a specified criteria.
- `SUM()` - returns the total sum of a numeric column.
- `MAX()` and `MIN()` - returns the largest/smallest value of the selected column.
- `GROUP BY` and `HAVING` – groups the result-set by one or more columns.
- `UCASE` and `LCASE` - converts the value of a field to uppercase/lowercase.
- `LEN()` - returns the length of the value in a text field.
- `ROUND()` - used to round a numeric field to the specified number of decimals.

Copy with Headers:

- On the result screen for a query – right click the top left corner and select ‘Copy with Headers’.
- This allows you to copy the table (with column names!) for use in a program like Excel.

### Date Functions

### NULL

---

## Exercises

---

## Wrap Up

---

## Query Tips

- When writing longer queries, it is easier to break the query onto multiple lines, as in the example above. This makes it easier to spot errors, and provides a visual break.
- Some SQL tools will perform a sanity check on your query, and notify you of some types of error.
- SQL is _very_ literal, and will perform exactly as asked – if there is a typo in your query, it could error or have unintended consequences.
