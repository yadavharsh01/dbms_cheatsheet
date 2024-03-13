# dbms_cheatsheet

### **What is Database?** 
A database is an organised collection of structured information, or data, typically stored electronically in a computer system. A database is usually controlled by a database management system (DBMS). Together, the data and the DBMS, along with the applications that are associated with them, are referred to as a database system, often shortened to just a database.
### **What is DBMS ? Mention advantages..** 
Database Management System (DBMS) is a software for storing and retrieving users’ data while considering appropriate security measures. It consists of a group of programs which manipulate the database. The DBMS accepts the request for data from an application and instructs the operating system to provide the specific data. In large systems, a DBMS helps users and other third-party software to store and retrieve data.

Advantages:

Improved data sharing
Improved data security
Better data integration
Minimised data inconsistency
Improved data access
Improved decision making
Improved end-user productivity
### **What is a database system?** 
A database management system (or DBMS) is essentially nothing more than a computerized data-keeping system. Users of the system are given facilities to perform several kinds of operations on such a system for either manipulation of the data in the database or the management of the database structure itself.
### **What is RDBMS ? Properties..** 
A Relational Database Management system (RDBMS) is a database management system that is based on the relational model. It has the following major components: Table, Record/Tuple/Row, Field, and Column/Attribute. Examples of the most popular RDBMS are MYSQL, Oracle, IBM DB2, and Microsoft SQL Server database.

Relational databases have the following properties:

Values are atomic.
All of the values in a column have the same data type.
Each row is unique.
The sequence of columns is insignificant.
The sequence of rows is insignificant.
Each column has a unique name.
Integrity constraints maintain data consistency across multiple tables.

### **Types of database languages** 
Data Definition Language: DDL stands for Data Definition Language. It is used to define database structure or pattern.
Data Manipulation Language: DML stands for Data Manipulation Language. It is used for accessing and manipulating data in a database. It handles user requests.
Data Control Language: DCL stands for Data Control Language. It is used to retrieve the stored or saved data.
Transaction Control Language: TCL is used to run the changes made by the DML statement. TCL can be grouped into a logical transaction.
### **ACID properties (VVVVV IMP)** 
To ensure the consistency of the database, certain properties are followed by all the
transactions occurring in the system.
These properties are called ACID Properties of a transaction.

Atomicity
Consistency
Isolation
Durability
### **Difference between vertical and horizontal scaling** 
Scaling alters the size of a system. In the scaling process, we either compress or expand the system to meet the expected needs. The scaling operation can be achieved by adding resources to meet the smaller expectation in the current system, or by adding a new system in the existing one, or both.

Vertical scaling keeps your existing infrastructure but adds computing power. Your existing pool of code does not need to change — you simply need to run the same code on machines with better specs. By scaling up, you increase the capacity of a single machine and increase its throughput. Vertical scaling allows data to live on a single node, and scaling spreads the load through CPU and RAM resources for your machines.

Horizontal scaling simply adds more instances of machines without first implementing improvements to existing specifications. By scaling out, you share the processing power and load balancing across multiple machines.
### **What is sharding** 
Sharding is a method of splitting and storing a single logical dataset in multiple databases. By distributing the data among multiple machines, a cluster of database systems can store larger dataset and handle additional requests. Sharding is necessary if a dataset is too large to be stored in a single database. Moreover, many sharding strategies allow additional machines to be added. Sharding allows a database cluster to scale along with its data and traffic growth.
### **Keys in DBMS**
A key is a set of attributes that can identify each tuple uniquely in the given relation.

Types of Keys:

Super Key – A superkey is a set of attributes that can identify each tuple uniquely in the given relation. A super key may consist of any number of attributes.
Candidate Key – A set of minimal attribute(s) that can identify each tuple uniquely in the given relation is called a candidate key.
Primary Key – A primary key is a candidate key that the database designer selects while designing the database. Primary Keys are unique and NOT NULL.
Alternate Key – Candidate keys that are left unimplemented or unused after implementing the primary key are called alternate keys.
Foreign Key – An attribute ‘X’ is called as a foreign key to some other attribute ‘Y’ when its values are dependent on the values of attribute ‘Y’. The relation in which attribute ‘Y’ is present is called the referenced relation. The relation in which attribute ‘X’ is present is called the referencing relation.
Composite Key – A primary key composed of multiple attributes and not just a single attribute is called a composite key.
Unique Key – It is unique for all the records of the table. Once assigned, its value cannot be changed i.e. it is non-updatable. It may have a NULL value. 
### **Types of relationship** 
A relationship is defined as an association among several entities.

Unary Relationship Set – Unary relationship set is a relationship set where only one entity set participates in a relationship set.
Binary Relationship Set – Binary relationship set is a relationship set where two entity sets participate in a relationship set.
Ternary Relationship Set – Ternary relationship set is a relationship set where three entity sets participate in a relationship set.
N-ary Relationship Set – N-ary relationship set is a relationship set where ‘n’ entity sets participate in a relationship set.
### **Data abstraction in DBMS, three levels of it** 
Data Abstraction is a process of hiding unwanted or irrelevant details from the end user. It provides a different view and helps in achieving data independence which is used to enhance the security of data.

Database systems include complex data-structures. In terms of retrieval of data, reduce complexity in terms of usability of users and in order to make the system efficient, developers use levels of abstraction that hide irrelevant details from the users. Levels of abstraction simplify database design.
### **Indexing in DBMS** 
Indexing is a way to optimise the performance of a database by minimising the number of disk accesses required when a query is processed. It is a data structure technique which is used to quickly locate and access the data in a database.
### **What is DDL (Data Definition Language)** 
DDL stands for Data Definition Language. It is used to define database structure or pattern.
It is used to create schema, tables, indexes, constraints, etc. in the database.
Using the DDL statements, you can create the skeleton of the database.
Data definition language is used to store the information of metadata like the number of tables and schemas, their names, indexes, columns in each table, constraints, etc.
### **What is DML (Data Manipulation Language)**
DML stands for Data Manipulation Language. It is used for accessing and manipulating data in a database. It handles user requests.
### **What is normalization ? Types of normalization.**
Normalization is the process of organizing data by disintegrating bigger table into smaller one’s
with proper dependencies
Redundant Data wastes a lot of disk space and creates maintenance problems (Update, Insert and Delete Anomaly). Hence the DB tables should be Normalized.
The process of Normalization is achieved by following some rules which are defined as Normal Forms
There are basically 3 types of Normal Form – 1NF, 2NF, 3NF. Strictness increases as we go from 1NF to 3NF.
Apart from the above mentioned Normal Form there exist one more Form called Boyce Codd Normal Form (BCNF) . This is an advanced version of 3NF and is even stricter than 3NF.
### **What is denormalization ?** 
Denormalization is a database optimization technique in which we add redundant data to one or more tables. This can help us avoid costly joins in a relational database. Note that denormalization does not mean not doing normalisation. It is an optimization technique that is applied after doing normalisation.
### **What is functional dependency ?** 
A functional dependency is a constraint that specifies the relationship between two sets of attributes where one set can accurately determine the value of other sets. It is denoted as X → Y, where X is a set of attributes that is capable of determining the value of Y. The attribute set on the left side of the arrow, X is called Determinant, while on the right side, Y is called the Dependent.
### **E-R Model ?** 
ER model stands for an Entity-Relationship model. It is a high-level data model. This model is used to define the data elements and relationship for a specified system.

It develops a conceptual design for the database. It also develops a very simple and easy to design view of data.
In ER modelling, the database structure is portrayed as a diagram called an entity-relationship diagram.
### **Conflict Serializability in DBMS ..** 
Serializability is a concept that helps us to check which schedules are serializable. A serializable schedule is the one that always leaves the database in consistent state.

A schedule is called conflict serializability if after swapping of non-conflicting operations, it can transform into a serial schedule. The schedule will be a conflict serializable if it is conflict equivalent to a serial schedule.
### **What is CCP ? (Concurrency Control Protocols)** 
Concurrency Control is the management procedure that is required for controlling concurrent execution of the operations that take place on a database.

The concurrency control protocols ensure the atomicity, consistency, isolation, durability and serializability of the concurrent execution of the database transactions.

Therefore, these protocols are categorised as:

Lock Based Concurrency Control Protocol
Timestamp Concurrency Control Protocol
Validation Based Concurrency Control Protocol
### **Entity, Entity Type, Entity Set, Weak Entity Set..** 
Entity in DBMS can be a real-world object with an existence, For example, in a College database, the entities can be Professor, Students, Courses, etc.

The entity type is a collection of the entity having similar attributes.

Types of Entity type:

Strong Entity Type:Strong entities are those entity types which have a key attribute. The primary key helps in identifying each entity uniquely. It is represented by a rectangle.
Weak Entity Type: Weak entity type doesn’t have a key attribute. Weak entity types can’t be identified on their own. It depends upon some other strong entity for its distinct identity.
Entity Set: Entity Set is a collection of entities of the same entity type. We can say that entity type is a superset of the entity set as all the entities are included in the entity type.
### **What are SQL commands ? Types of them..** 
SQL commands are instructions. It is used to communicate with the database. It is also used to perform specific tasks, functions, and queries of data.
SQL can perform various tasks like create a table, add data to tables, drop the table, modify the table, set permission for users.
Types of SQL Commands
There are five types of SQL commands: DDL, DML, DCL, TCL, and DQL.


DBMS SQL command
1. Data Definition Language (DDL)
DDL changes the structure of the table like creating a table, deleting a table, altering a table, etc.
All the command of DDL are auto-committed that means it permanently save all the changes in the database.
Here are some commands that come under DDL:

CREATE
ALTER
DROP
TRUNCATE
a. CREATE It is used to create a new table in the database.

Syntax:

CREATE TABLE TABLE_NAME (COLUMN_NAME DATATYPES[,....]);  
Example:

CREATE TABLE EMPLOYEE(Name VARCHAR2(20), Email VARCHAR2(100), DOB DATE);  
b. DROP: It is used to delete both the structure and record stored in the table.

Syntax

DROP TABLE table_name;  
Example

DROP TABLE EMPLOYEE;  
c. ALTER: It is used to alter the structure of the database. This change could be either to modify the characteristics of an existing attribute or probably to add a new attribute.

Syntax:

To add a new column in the table

ALTER TABLE table_name ADD column_name COLUMN-definition;    
To modify existing column in the table:

ALTER TABLE table_name MODIFY(column_definitions....);  
EXAMPLE

ALTER TABLE STU_DETAILS ADD(ADDRESS VARCHAR2(20));  
ALTER TABLE STU_DETAILS MODIFY (NAME VARCHAR2(20));  
d. TRUNCATE: It is used to delete all the rows from the table and free the space containing the table.

Syntax:

TRUNCATE TABLE table_name;  
Example:

TRUNCATE TABLE EMPLOYEE;  
2. Data Manipulation Language
DML commands are used to modify the database. It is responsible for all form of changes in the database.
The command of DML is not auto-committed that means it can't permanently save all the changes in the database. They can be rollback.
Here are some commands that come under DML:

INSERT
UPDATE
DELETE
a. INSERT: The INSERT statement is a SQL query. It is used to insert data into the row of a table.

Syntax:

INSERT INTO TABLE_NAME    
(col1, col2, col3,.... col N)  
VALUES (value1, value2, value3, .... valueN);  
Or

INSERT INTO TABLE_NAME    
VALUES (value1, value2, value3, .... valueN);    
For example:

INSERT INTO javatpoint (Author, Subject) VALUES ("Sonoo", "DBMS");  
b. UPDATE: This command is used to update or modify the value of a column in the table.

Syntax:

UPDATE table_name SET [column_name1= value1,...column_nameN = valueN] [WHERE CONDITION]   
For example:

UPDATE students    
SET User_Name = 'Sonoo'    
WHERE Student_Id = '3'  
c. DELETE: It is used to remove one or more row from a table.

Syntax:

DELETE FROM table_name [WHERE condition];  
For example:

DELETE FROM javatpoint  
WHERE Author="Sonoo";  
3. Data Control Language
DCL commands are used to grant and take back authority from any database user.

Here are some commands that come under DCL:

Grant
Revoke
a. Grant: It is used to give user access privileges to a database.

Example

GRANT SELECT, UPDATE ON MY_TABLE TO SOME_USER, ANOTHER_USER;  
b. Revoke: It is used to take back permissions from the user.

Example

REVOKE SELECT, UPDATE ON MY_TABLE FROM USER1, USER2;  
4. Transaction Control Language
TCL commands can only use with DML commands like INSERT, DELETE and UPDATE only.

These operations are automatically committed in the database that's why they cannot be used while creating tables or dropping them.

Here are some commands that come under TCL:

COMMIT
ROLLBACK
SAVEPOINT
a. Commit: Commit command is used to save all the transactions to the database.

Syntax:

COMMIT;  
Example:

DELETE FROM CUSTOMERS  
WHERE AGE = 25;  
COMMIT;  
b. Rollback: Rollback command is used to undo transactions that have not already been saved to the database.

Syntax:

ROLLBACK;  
Example:

DELETE FROM CUSTOMERS  
WHERE AGE = 25;  
ROLLBACK;  
c. SAVEPOINT: It is used to roll the transaction back to a certain point without rolling back the entire transaction.

Syntax:

SAVEPOINT SAVEPOINT_NAME;  
5. Data Query Language
DQL is used to fetch the data from the database.

It uses only one command:

SELECT
a. SELECT: This is the same as the projection operation of relational algebra. It is used to select the attribute based on the condition described by WHERE clause.

Syntax:

SELECT expressions    
FROM TABLES    
WHERE conditions;  
For example:

SELECT emp_name  
FROM employee  
WHERE age > 20;  

### **Nested Queries in SQL ?** 
A nested query is a query that has another query embedded within it. The embedded query is called a subquery.

A subquery typically appears within the WHERE clause of a query. It can sometimes appear in the FROM clause or HAVING clause.

Example
Let’s learn about nested queries with the help of an example.

Find the names of employee who have regno=103

The query is as follows −

select E.ename from employee E where E.eid IN (select S.eid from salary S where S.regno=103);

### **What is JOIN .. Explain types of JOINs** 
JOIN means to combine something. In case of SQL, JOIN means "to combine two or more tables".

In SQL, JOIN clause is used to combine the records from two or more tables in a database.

Types of SQL JOIN
INNER JOIN
LEFT JOIN
RIGHT JOIN
FULL JOIN
Sample Table
EMPLOYEE

EMP_ID	EMP_NAME	CITY	SALARY	AGE
1	Angelina	Chicago	200000	30
2	Robert	Austin	300000	26
3	Christian	Denver	100000	42
4	Kristen	Washington	500000	29
5	Russell	Los angels	200000	36
6	Marry	Canada	600000	48
PROJECT

PROJECT_NO	EMP_ID	DEPARTMENT
101	1	Testing
102	2	Development
103	3	Designing
104	4	Development
1. INNER JOIN
In SQL, INNER JOIN selects records that have matching values in both tables as long as the condition is satisfied. It returns the combination of all rows from both the tables where the condition satisfies.

Syntax

SELECT table1.column1, table1.column2, table2.column1,....  
FROM table1   
INNER JOIN table2  
ON table1.matching_column = table2.matching_column;  
Query

SELECT EMPLOYEE.EMP_NAME, PROJECT.DEPARTMENT   
FROM EMPLOYEE  
INNER JOIN PROJECT  
ON PROJECT.EMP_ID = EMPLOYEE.EMP_ID;  
Output

EMP_NAME	DEPARTMENT
Angelina	Testing
Robert	Development
Christian	Designing
Kristen	Development
2. LEFT JOIN
The SQL left join returns all the values from left table and the matching values from the right table. If there is no matching join value, it will return NULL.

Syntax

SELECT table1.column1, table1.column2, table2.column1,....  
FROM table1   
LEFT JOIN table2  
ON table1.matching_column = table2.matching_column;  
Query

SELECT EMPLOYEE.EMP_NAME, PROJECT.DEPARTMENT   
FROM EMPLOYEE  
LEFT JOIN PROJECT  
ON PROJECT.EMP_ID = EMPLOYEE.EMP_ID;  
Output

EMP_NAME	DEPARTMENT
Angelina	Testing
Robert	Development
Christian	Designing
Kristen	Development
Russell	NULL
Marry	NULL
3. RIGHT JOIN
In SQL, RIGHT JOIN returns all the values from the values from the rows of right table and the matched values from the left table. If there is no matching in both tables, it will return NULL.

Syntax

SELECT table1.column1, table1.column2, table2.column1,....  
FROM table1   
RIGHT JOIN table2  
ON table1.matching_column = table2.matching_column;  
Query

SELECT EMPLOYEE.EMP_NAME, PROJECT.DEPARTMENT   
FROM EMPLOYEE  
RIGHT JOIN PROJECT  
ON PROJECT.EMP_ID = EMPLOYEE.EMP_ID;  
Output

EMP_NAME	DEPARTMENT
Angelina	Testing
Robert	Development
Christian	Designing
Kristen	Development
4. FULL JOIN
In SQL, FULL JOIN is the result of a combination of both left and right outer join. Join tables have all the records from both tables. It puts NULL on the place of matches not found.

Syntax

SELECT table1.column1, table1.column2, table2.column1,....  
FROM table1   
FULL JOIN table2  
ON table1.matching_column = table2.matching_column;  
Query

SELECT EMPLOYEE.EMP_NAME, PROJECT.DEPARTMENT   
FROM EMPLOYEE  
FULL JOIN PROJECT   
ON PROJECT.EMP_ID = EMPLOYEE.EMP_ID;  
Output

EMP_NAME	DEPARTMENT
Angelina	Testing
Robert	Development
Christian	Designing
Kristen	Development
Russell	NULL
Marry	NULL

### **Inner and Outer Join** 
Here are the different types of the JOINs in SQL:
(INNER) JOIN: Returns records that have matching values in both tables
LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table
### **Diff between 2 tier and 3 tier architecture** 
 Two-Tier Database Architecture – In two-tier, the application logic is either buried inside the User Interface on the client or within the database on the server (or both). With two-tier client/server architectures, the user system interface is usually located in the user’s desktop environment and the database management services are usually in a server that is a more powerful machine that services many clients. 
Three-Tier Database Architecture – In three-tier, the application logic or process lives in the middle-tier, it is separated from the data and the user interface. Three-tier systems are more scalable, robust and flexible. In addition, they can integrate data from multiple sources. In the three-tier architecture, a middle tier was added between the user system interface client environment and the database management server environment. There are a variety of ways of implementing this middle tier, such as transaction processing monitors, message servers, or application servers.

### **Diff between TRUNCATE and DELETE command ..** 
DELETE is a DML(Data Manipulation Language) command and is used when we specify the row (tuple) that we want to remove or delete from the table or relation. The DELETE command can contain a WHERE clause. If the WHERE clause is used with the DELETE command, then it removes or deletes only those rows (tuples) that satisfy the condition; otherwise, by default, it removes all the tuples (rows) from the table. Remember that DELETE logs the row deletions.

Syntax:

DELETE FROM TableName

WHERE condition;

posterposter 
TRUNCATE is a DDL(Data Definition Language) command and is used to delete all the rows or tuples from a table. Unlike the DELETE command, the TRUNCATE command does not contain a WHERE clause. In the TRUNCATE command, the transaction log for each deleted data page is not recorded. Unlike the DELETE command, the TRUNCATE command is fast. We cannot roll back the data after using the TRUNCATE command. 

Syntax:

TRUNCATE TABLE TableName;
### **Difference between Intension and Extension in a DataBase**
	Intension Database	
	The intension corresponds to what is specified in the relational schema. The intension thus defines all permissible extensions.
	The intension of a given relation is independent of time. It is the permanent part of the relationship.
	The intension is a combination of two things: a structure and a set of integrity constraints.	
Example of Intension Database

Employee (Reg  No.(5) Not NULL, Name Char(20), Age Number (2), Company Char(20))
This is the intension of employee relation.
    
    Extension Database
	The extension of a given relation is the set of tuples appearing in that relationship at any given instance
	The intension of a given relation is independent of time. It is the permanent part of the relationship.
    It changes as tuples are created, destroyed, and updated.

Example of Extension Database

Relation: Extension of employees at time t1 when 2 tuples are added-

Reg No.	Name	Age 	Company
22501	Sonakshi Sahni	27	Yagesh Export Ltd.
22502	Sneha Sarin	30	Smile Crafters Dental Cooperates

### **Difference between share lock and exclusive lock, definition of lock** 
One of the method to ensure isolation property in transaction is to require data items be accessed in a mutually exclusive manner. That means, while one transaction is accessing a data item, no other transaction can modify that data item. So, the most common method used to implement requirement is to allow a transaction to access a data item only if it is currently holding a lock on that item. Thus, the lock on operation is required to ensure isolation of transaction. 

 Shared Lock (S):

Another transaction that tries to read the same data is permitted to read, but a transaction that tries to update the data will be prevented from doing so until the shared lock is released.
Shared lock is also called read lock, used for reading data items only.
Shared locks support read integrity. They ensure that a record is not in process of being updated during a read-only request.
Shared locks can also be used to prevent any kind of updates of record.
It is denoted by Lock-S.
S-lock is requested using Lock-S instruction.
For example, consider a case where initially A=100 and there are two transactions which are reading A. If one of transaction wants to update A, in that case other transaction would be reading wrong value. However, Shared lock prevents it from updating until it has finished reading. 

Exclusive Lock (X) :

When a statement modifies data, its transaction holds an exclusive lock on data that prevents other transactions from accessing the data.
This lock remains in place until the transaction holding the lock issues a commit or rollback.
They can be owned by only one transaction at a time.
With the Exclusive Lock, a data item can be read as well as written. Also called write lock.
 Any transaction that requires an exclusive lock must wait if another transaction currently owns an exclusive lock or a shared lock against the requested resource.
They can be owned by only one transaction at a time.
It is denoted as Lock-X.
X-lock is requested using Lock-X instruction.
