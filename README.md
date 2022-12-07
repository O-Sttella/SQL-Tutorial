# SQL-Tutorial
Learn SQL by Stella

## Tutorial

---

### [1-SQL TUTORIAL-W3SCHOOLS](https://www.w3schools.com/sql/)

+KEYWORDS

<details>
    <summary>1. What is SQL?</summary>

```bs
SQL is a standard language for accessing and manipulating databases.
```

```bs
-SQL stands for Structured Query Language
-SQL lets you access and manipulate databases
-SQL became a standard of the American National Standards Institute (ANSI) in 1986, and of the International Organization for Standardization (ISO) in 1987
```

</details>

<details>
    <summary>2. Select all from Table</summary>

```bs
SELECT * FROM Customers;
```

</details>

<details>
    <summary>3. Select multiple columns from Table</summary>

```bs
SELECT CustomerName, City FROM Customers;
```

</details>

<details>
    <summary>4. Select DISTINCT - Without Duplicates</summary>

```bs
SELECT DISTINCT Country FROM Customers;
```

```bs
SELECT COUNT(DISTINCT Country) FROM Customers;
```

</details>

<details>
    <summary>5. SQL WHERE CLAUSE</summary>

```bs
The WHERE Clause is used to filter data. It can be combined with numerical, logical operators and the LIKE, BETWEEN and IN clauses. 

SELECT column1, column2, ...
FROM table_name
WHERE condition;

Operator	Description	Example
=	Equal	
>	Greater than	
<	Less than	
>=	Greater than or equal	
<=	Less than or equal	
<>	Not equal. Note: In some versions of SQL this operator may be written as !=	
BETWEEN	Between a certain range	
LIKE	Search for a pattern	
IN	To specify multiple possible values for a column

## The SQL AND, OR and NOT Operators

The AND operator displays a record if all the conditions separated by AND are TRUE.
The OR operator displays a record if any of the conditions separated by OR is TRUE.
The NOT operator displays a record if the condition(s) is NOT TRUE.

SELECT * FROM Customers
WHERE City='Berlin' OR City='München';

NOTE THAT this examplw also applies to AND & NOT. However, the IN clause is used when you dont want to use multiple OR in the code. The example for NOT is given below.

SELECT * FROM Customers
WHERE NOT Country='Germany';

THEY CAN ALSO BE COMBINED

SELECT * FROM Customers
WHERE Country='Germany' AND (City='Berlin' OR City='München');

SQL ORDER BY and LIMIT KEY WORDS

The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword. NOTE THAT multiple columns can be ordered in one code. 
The LIMIT keyword specifies how many of the ordered values to be returned. 

SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;
LIMIT 5

SQL INSERT INTO KEYWORD

It is possible to write the INSERT INTO statement in two ways:
Specify both the column names and the values to be inserted:

INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');

One can also INSERT INTO specific columns. However, you must ensure the column position and value to be inserted align. Example is also seen below:
INSERT INTO Customers (CustomerName, City, Country)
VALUES ('Cardinal', 'Stavanger', 'Norway');


SQL NULL VALUES

A field with a NULL value is a field with no value.
If a field in a table is optional, it is possible to insert a new record or update a record without adding a value to this field. Then, the field will be saved with a NULL value.

Note: A NULL value is different from a zero value or a field that contains spaces. A field with a NULL value is one that has been left blank during record creation!
Also important to note that NULL can not be used along with comparison operators. Instead we use the IS NULL and IS NOT NULL syntax to determine if a column or table is NULL or NOT

The IS NULL Operator
The IS NULL operator is used to test for empty values (NULL values).
The following SQL lists all customers with a NULL value in the "Address" field:

Example
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NULL;

The IS NOT NULL Operator
The IS NOT NULL operator is used to test for non-empty values (NOT NULL values).
The following SQL lists all customers with a value in the "Address" field:

Example
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NOT NULL;

SQL UPDATE STATEMENT

The UPDATE statement is used to modify the existing records in a table.

UPDATE Syntax

UPDATE Customers
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE CustomerID = 1;

Note: Be careful when updating records in a table! Notice the WHERE clause in the UPDATE statement. The WHERE clause specifies which record(s) that should be updated. If you omit the WHERE clause, all records in the table will be updated! It can be used to update single or mutiple columns. 

UPDATE Multiple Records
It is the WHERE clause that determines how many records will be updated.
The following SQL statement will update the ContactName to "Juan" for all records where country is "Mexico":

Example
UPDATE Customers
SET ContactName='Juan'
WHERE Country='Mexico';



Excel -> File -> Export -
```

```bs

```

</details>

<details>
    <summary>6. sample</summary>

```bs

```

```bs

```

</details>

<details>
    <summary>7. sample</summary>

```bs

```

```bs

```

</details>

<details>
    <summary>8. sample</summary>

```bs

```

```bs

```

</details>

<details>
    <summary>9. sample</summary>

```bs

```

```bs

```

</details>

<details>
    <summary>10. sample</summary>

```bs

```

```bs

```

</details>


