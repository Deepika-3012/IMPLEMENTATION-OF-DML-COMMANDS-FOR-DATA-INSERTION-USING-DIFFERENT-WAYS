# IMPLEMENTATION-OF-DML-COMMANDS-FOR-DATA-INSERTION-USING-DIFFERENT-WAYS
AIM:

To implement commands for data insertion using different ways, integrity constraints and
truncate commands

PROCEDURE:

1.DIFERENT WAYS TO INSERT A DATA INTO TABLE:

Method 1: The first way specifies both the column names and the values to be inserted.

Syntax:
INSERT INTO table-name (column-names) VALUES (values) ;

Method 2: Insert Data Only in Specified Columns.

Method 3: If you are adding the values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table.

2.INTEGRITY CONSTRAINTS:

• The Set of rules which is used to maintain the quality of information are known as
integrity constraints.

• Integrity constraints make sure about data intersection, update and so on.

• Integrity constraints can be understood as a guard against unintentional damage to the
database.

Domain Constraint

• The Definition of an applicable set of values is known as domain constraint.

• Strings, character, time, integer, currency, date etc. Are examples of the data type of domain constraints

Entity Integer Constraint

• Entity Integrity Constraints states that the primary value key cannot be null because the primary value key is used to find out individual rows in relation and if the value of the primary key is null then it is not easy to identify those rows.

• There can be a null value in the table apart from the primary key field.

Referential Integrity Constraint

1. Referential Integrity Constraint is specific between two tables.

2. A foreign key in the 1st table refers to the primary key of the 2nd table, in this case
each value of the foreign key in the 1st table has to be null or present in the 2nd table.

Key Constraints

• The Entity within its entity set is identified uniquely by the key which is the entity set.

• There can be a number of keys in an entity set but only one will be the primary key
out of all keys. In a relational table a primary key can have a unique as well as a null
value.

3.TRUNCATE :

TRUNCATE command removes all the records from a table. But this command will not destroy the table's structure. When we use TRUNCATE command on a table its (auto-increment) primary key is also initialized.

Syntax:

TRUNCATE TABLE table_name;

Example:

TRUNCATE TABLE EMPLOYEE;

COMMANDS:

SQL>CREATE DATABASE Organization;

Database Created

SQL>CREATE TABLE Persons
(
PersonID int,
LastName varchar(255),
FirstName varchar(255),
Address varchar(255),
City varchar(255)
);

SQL>INSERT INTO Persons (PersonID, LastName, FirstName, Address, City) VALUES('101', 'Erichsen', 'Tom', 'Street no-21', 'New York');

SQL>INSERT INTO Persons (PersonID, LastName, FirstName, Address, City)VALUES ('102', 'Johnson', 'Marry', 'Old Street Road-43', 'California');

SQL>INSERT INTO Persons (PersonID, LastName,FirstName)VALUES ('103', 'Steve','Rossy')

SQL>INSERT INTO Persons VALUES ('104', 'Allen', 'Ketty', 'South Side Road', 'U.S.');

SQL>select * from persons

SQL> TRUNCATE TABLE Persons;

SQL>SELECT * FORM Persons;

Empty set (0.00 sec)

SQL> CREATE TABLE customer_details(customer_id character varying(255) NOT NULL,cutomer_name character varying(255) NOT NULL,quantity integer NOT NULL,date_purchased date);

Table Created.

SQL> INSERT INTO public.customer_details(customer_id, customer_name, quantity, date_purchased)VALUES ('US1002','Kabir Khan','ABC', 2019-12-31);

SQL> CREATE TABLE Students(Student_ID int NOT NULL,Student_Name varchar(255) NOT NULL,Class_Name varchar(255) UNIQUE,Age int PRIMARY KEY (Student_ID));

Table Created.

SQL> INSERT INTO public.students(student_id, student_name, class_name, age)VALUES (32,'ABC','V',12),(32,'XYZ','V',11);

SQL> CREATE TABLE Department(Department_ID int NOT NULL,Department_Name varchar(255) NOT NULL,PRIMARY KEY(Department_ID));

SQL>CREATE TABLE Employees(Employee_ID int NOT NULL,Employee_Name varchar(255) NOT NULL,Department int NOT NULL,Age int,FOREIGN KEY (Department) REFERENCES Department(Department_ID));

Table Created.

SQL> INSERT INTO public.employees(employee_id, employee_name, department, age)VALUES (1002,'K K Davis',10,43);


