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


