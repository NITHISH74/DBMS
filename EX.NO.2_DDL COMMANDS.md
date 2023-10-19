# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb

### SQL QUERY:
```sql
Create a database studentdb;
```
### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/3c8a12ec-b1c0-45ee-88d4-ccd5c73bbc84)


### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```sql
 create table student(rollno int,name char(20),age int,address varchar(20),phoneno int);
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/fb653ac4-abdb-4f23-9760-ecfcc3ad9670)

### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
```sql
alter table student add department char(30);
```
### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/be917502-6e7a-4cff-a0f6-8b02db1bdcf6)

### 4) Drop the mystudent table

### SQL QUERY: 

```sql
drop table student;
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/068bedc3-28c7-4a08-8be3-0b36bca488eb)

### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```sql
truncate table student;
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/9035ad47-2e91-4788-b563-b4d29d7d78e4)

### 6) Rename the student table to mystudent
 
### SQL QUERY: 
```sql
alter table student rename to mystudent;
```

### OUTPUT:

![image](https://github.com/NITHISH74/DBMS/assets/94164665/ad411f19-e8e6-4b21-a554-14bcc4210a03)


## Result:
Thus the basic DDL commands in SQL are executed. 


