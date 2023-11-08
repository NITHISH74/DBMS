# Ex. No: 8 PL/SQL program using Cursor 
### DATE: 
## AIM: 
To create PL/SQL program to display the customer table 
## Algorithms:
### Step 01:
Declare the variable  in Declare section.
### Step 02:
Fetch the variable with datatype similar to data type in cursor 
### Step 03:
Create a cursor to select all rows from customers table.
### Step 04:
Display the result 
### Step 05:
End the begin section.

## Program:
### Create employee table:
```sql
CREATE TABLE employd (
  empid NUMBER,
  empname VARCHAR(10),
  dept VARCHAR(10),
  salary NUMBER
);

INSERT INTO employd VALUES (1, 'Gojo', 'HR', 100000);
INSERT INTO employd VALUES (2, 'Yuji', 'Sales', 80000);
select * from employd;
```


### PLSQL Cursor code:
```sql
DECLARE
   CURSOR employd_cursor IS
   SELECT empid,empname,dept,salary
   FROM employd;
   emp_id NUMBER;
   emp_name VARCHAR(50);
   emp_dept VARCHAR(50);
   emp_salary NUMBER;
BEGIN
  OPEN employd_cursor;

  LOOP
    FETCH employd_cursor INTO emp_id, emp_name, emp_dept, emp_salary;

    EXIT WHEN employd_cursor%NOTFOUND;

    DBMS_OUTPUT.PUT_LINE('Employee ID: ' || emp_id);
    DBMS_OUTPUT.PUT_LINE('Employee Name: ' || emp_name);
    DBMS_OUTPUT.PUT_LINE('Department: ' || emp_dept);
    DBMS_OUTPUT.PUT_LINE('Salary: ' || emp_salary);
  END LOOP;

  CLOSE employd_cursor;
END;
/
```

## Output:
![image](https://github.com/Lakshmipriya2005/DBMS/assets/115525361/d08431a3-089d-449d-809c-785120d2b818)

## Result:
Thust the program was performed sucessfully.
