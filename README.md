# SQL
SQL (Structured Query Language) is a programming language designed for managing and manipulating relational databases.

*Database*

Database is collection of data in a format that can be easily accessed(Digital)
<br>
A software application used to manage our DB is called DBMS (Database Management System)

*Types of Database*

Relational Databases-MySQL
<br>
Non-relational(NoSQL) Databases- mongoDB

## We Use SQL programming language to interact with relational databases
It is used to perform <b>CRUD</b> operations:
Create <br>
Read <br>
Update <br>
Delete <br>

```sql
CREATE DATABASE db_name;
DROP DATABASE db_name;
```
## Creating our first Table
```sql
USE db_name;

CREATE TABLE table_name(
column_name1 datatype constraint;
column_name2 datatype constraint;
column_name3 datatype constraint;
```

## Types of SQL Commands
DDL(Data Definition Language): create, alter, rename, truncate & drop

DQL(Data Query Language): select

DML(Data Modification Language): select, insertm update & delete

DCL(Data Control Language): grant and revoke

TCL(Transaction Control Language): start transaction, commit, rollback etc
