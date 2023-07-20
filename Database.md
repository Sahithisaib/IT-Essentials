# Database

A database is an organized collection of structured information, or data, typically stored electronically in a computer system. A database is usually controlled by a database management system (DBMS). 

SQL: SQL is a programming language used by nearly all relational databases to query, manipulate, and define data, and to provide access control.

A database typically requires a comprehensive database software program known as a database management system (DBMS). A DBMS serves as an interface between the database and its end users or programs, allowing users to retrieve, update, and manage how the information is organized and optimized. 

Commands:
--

Creating a table:

CREATE TABLE TableName (

Column1 datatype,

Column2 datatype,

Column3 datatype,

....

ColumnN datatype
);

Creating a table with "As":

CREATE TABLE NewTableName AS

SELECT Column1, column2,..., ColumnN

FROM ExistingTableName

WHERE ....;

DROP a table:

DROP TABLE TableName;

Truncate a table:

Truncate TABLE TableName;

Alter table ADD:

ALTER TABLE TableName

ADD ColumnName Datatype;

Alter table DROP:


ALTER TABLE TableName

DROP COLUMN ColumnName;

Backup a database:

BACKUP DATABASE DatabaseName

TO DISK = 'filepath';

**SQL Constraints:**

Not Null: A column cannot have null values.

Example:

CREATE TABLE Employee_Info(

EmployeeID int NOT NULL,

EmployeeName varchar(255) NOT NULL,

Emergency ContactName varchar(255),

PhoneNumber int NOT NULL,

Address varchar(255),

City varchar(255),

Country varchar(255)
);


Unique: Ensure all values in column are unique.

CREATE TABLE Employee_Info(

EmployeeID int NOT NULL UNIQUE,

EmployeeName varchar(255) NOT NULL,

Emergency ContactName varchar(255),

PhoneNumber int NOT NULL,

Address varchar(255),

City varchar(255),

Country varchar(255)
);

UNIQUE on Multiple Columns:
 
CREATE TABLE Employee_Info
(

EmployeeID int NOT NULL,

EmployeeName varchar(255) NOT NULL,

Emergency ContactName varchar(255),

PhoneNumber int NOT NULL,

Address varchar(255),

City varchar(255),

Country varchar(255),

CONSTRAINT UC_Employee_Info UNIQUE(Employee_ID, PhoneNumber));

Check: Ensures that all the values in a column satisfy a specific condition.

CHECK Constraint on create table:
 
CREATE TABLE Employee_Info
(

EmployeeID int NOT NULL,

EmployeeName varchar(255),

Emergency ContactName varchar(255),

Country varchar(255) CHECK (Country=='India')
);

CHECK Constraint on alter table:
 
ALTER TABLE Employee_Info

ADD CHECK (Country=='India');

Default: Sets default values for a column when no value is specified.

CREATE TABLE Employee_Info
(

EmployeeID int NOT NULL,

City varchar(255),

Country varchar(255) DEFAULT 'India'
);

Index: INDEX is used to create indexes in the table, through which we can create and retrieve data from the database very quickly.

CREATE INDEX IndexName

ON TableName (Column1, Column2, ...ColumnN);

**Data Manipulation Commands**:

Use: To select database on which we want to perform operations.

Use Employee,

Insert into: Insert new records into the table.

INSERT INTO TableName (Column1, Column2, Column3, ...,ColumnN)

VALUES (value1, value2, value3, ...);

Update: Modify the existing records in the table.

UPDATE TableName

SET Column1 = Value1, Column2 = Value2, ...

WHERE Condition;

Delete: Delete the existing records in a table.

DELETE FROM TableName WHERE Condition;

Select: Select is used to select data from a database and the data returned is stored in a result table, called the result-set.

SELECT Column1, Column2, ...ColumN

FROM TableName;

