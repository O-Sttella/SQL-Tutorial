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

SQL DELETE Statement
The DELETE statement is used to delete existing records in a table.

DELETE Syntax
DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';

Note: Be careful when deleting records in a table! Notice the WHERE clause in the DELETE statement. The WHERE clause specifies which record(s) should be deleted. If you omit the WHERE clause, all records in the table will be deleted!

THE SQL TOP, LIMIT, FETCH FIRST AND ROWNUM Clause

The SQL SELECT TOP Clause
The SELECT TOP clause is used to specify the number of records to return.

The SELECT TOP clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.

Note: Not all database systems support the SELECT TOP clause. MySQL supports the LIMIT clause to select a limited number of records, while Oracle uses FETCH FIRST n ROWS ONLY and ROWNUM.

SQL Server / MS Access Syntax:

SELECT TOP number|percent column_name(s)
FROM table_name
WHERE condition;
MySQL Syntax:

SELECT column_name(s)
FROM table_name
WHERE condition
LIMIT number;
Oracle 12 Syntax:

SELECT column_name(s)
FROM table_name
ORDER BY column_name(s)
FETCH FIRST number ROWS ONLY;
Older Oracle Syntax:

SELECT column_name(s)
FROM table_name
WHERE ROWNUM <= number;
Older Oracle Syntax (with ORDER BY):

SELECT *
FROM (SELECT column_name(s) FROM table_name ORDER BY column_name(s))
WHERE ROWNUM <= number;

The SQL MIN() and MAX() Functions

The MIN() function returns the smallest value of the selected column.
The MAX() function returns the largest value of the selected column.

MIN() Syntax  [For a MAX question, simply replace MIN with MAX]
SELECT MIN(Price) AS SmallestPrice
FROM Products;

The SQL COUNT(), AVG() and SUM() Functions
The COUNT() function returns the number of rows that matches a specified criterion.

COUNT() Syntax
SELECT COUNT(column_name)
FROM table_name
WHERE condition;

The AVG() function returns the average value of a numeric column. 
AVG() Syntax
SELECT AVG(column_name)
FROM table_name
WHERE condition;

The SUM() function returns the total sum of a numeric column. 
SUM() Syntax
SELECT SUM(column_name)
FROM table_name
WHERE condition;


The SQL LIKE Operator

The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.

There are two wildcards often used in conjunction with the LIKE operator:

 The percent sign (%) represents zero, one, or multiple characters
 The underscore sign (_) represents one, single character
Note: MS Access uses an asterisk (*) instead of the percent sign (%), and a question mark (?) instead of the underscore (_).

The percent sign and the underscore can also be used in combinations!

LIKE Syntax
LIKE Operator	Description
WHERE CustomerName LIKE 'a%'	Finds any values that start with "a"
WHERE CustomerName LIKE '%a'	Finds any values that end with "a"
WHERE CustomerName LIKE '%or%'	Finds any values that have "or" in any position
WHERE CustomerName LIKE '_r%'	Finds any values that have "r" in the second position
WHERE CustomerName LIKE 'a_%'	Finds any values that start with "a" and are at least 2 characters in length
WHERE CustomerName LIKE 'a__%'	Finds any values that start with "a" and are at least 3 characters in length
WHERE ContactName LIKE 'a%o'	Finds any values that start with "a" and ends with "o"

LIKE SYNTAX EXAMPLE
SELECT * FROM Customers
WHERE CustomerName LIKE 'a%';


The SQL IN Operator

The IN operator allows you to specify multiple values in a WHERE clause.
The IN operator is a shorthand for multiple OR conditions.

IN Syntax
The following SQL statement selects all customers that are located in "Germany", "France" or "UK":

Example
SELECT * FROM Customers
WHERE Country IN ('Germany', 'France', 'UK');

The following SQL statement selects all customers that are from the same countries as the suppliers:

Example
SELECT * FROM Customers
WHERE Country IN (SELECT Country FROM Suppliers);


The SQL BETWEEN Operator

The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates.
The BETWEEN operator is inclusive: begin and end values are included. 

BETWEEN Syntax
he following SQL statement selects all products with a price between 10 and 20:

Example
SELECT * FROM Products
WHERE Price BETWEEN 10 AND 20;

NOT BETWEEN Example
To display the products outside the range of the previous example, use NOT BETWEEN: This means other prices within the 10 - 20 price range will not be returned. only those less than 10 and above 20 will be returned.

Example
SELECT * FROM Products
WHERE Price NOT BETWEEN 10 AND 20;


SQL Aliases 'AS'

SQL aliases are used to give a table, or a column in a table, a temporary name.
Aliases are often used to make column names more readable.
An alias only exists for the duration of that query. It doesnt change the column or table name in the database. Also the type of DBMS will determine how the syntax would be written
An alias is created with the AS keyword.

Alias Column Syntax
The following SQL statement creates two aliases, one for the CustomerID column and one for the CustomerName column:

Example
SELECT CustomerID AS ID, CustomerName AS Customer
FROM Customers;

The following SQL statement creates an alias named "Address" that combine four columns (Address, PostalCode, City and Country):

Example
SELECT CustomerName, Address + ', ' + PostalCode + ' ' + City + ', ' + Country AS Address
FROM Customers;

Note: To get the SQL statement above to work in MySQL use the following:

SELECT CustomerName, CONCAT(Address,', ',PostalCode,', ',City,', ',Country) AS Address
FROM Customers;
Note: To get the SQL statement above to work in Oracle use the following:

SELECT CustomerName, (Address || ', ' || PostalCode || ' ' || City || ', ' || Country) AS Address
FROM Customers;

Alias for Tables Example
The following SQL statement selects all the orders from the customer with CustomerID=4 (Around the Horn). We use the "Customers" and "Orders" tables, and give them the table aliases of "c" and "o" respectively (Here we use aliases to make the SQL shorter):

Example
SELECT o.OrderID, o.OrderDate, c.CustomerName
FROM Customers AS c, Orders AS o
WHERE c.CustomerName='Around the Horn' AND c.CustomerID=o.CustomerID;

The following SQL statement is the same as above, but without aliases:

Example
SELECT Orders.OrderID, Orders.OrderDate, Customers.CustomerName
FROM Customers, Orders
WHERE Customers.CustomerName='Around the Horn' AND Customers.CustomerID=Orders.CustomerID;

Aliases can be useful when:

There are more than one table involved in a query
Functions are used in the query
Column names are big or not very readable
Two or more columns are combined together


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


