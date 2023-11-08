# Ex. No: 11 DATA BASE CONNECTIVITY USING  MYSQL AND JAVA
### DATE: 
## AIM: 
To create database connectivity and display the employee table 
## Algorithms:
### Steps 01:
Install mysql,visual studio,jdk, extensions of java pack.
### Steps 02:
Create a employee table and insert the data into employee table  
### Steps 03:
Create a new java project in visual studio.
### Steps 04:
write a java progarm to perform the following 1.create a connection 2. fetch data and store it in result set 3. Display table rows. 4. Close the connection
### Steps 05:
Deploy the jar file in lib folder 
### Steps 06:
Run the program

## Program:
```sql
package com.employees;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;

public class App {
	public static void main(String[] args) throws SQLException {

		System.out.println("Connecting to DB");
		Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/mydb", "root", "Root@2005");

		System.out.println("Connection Successfull");

		Statement stmt = con.createStatement();
		ResultSet rs = stmt.executeQuery("Select * from employees");
		

		while (rs.next()) {
			System.out.println("id :" + rs.getInt("Emp_id"));
			System.out.println("name :" + rs.getString("Emp_name"));
			System.out.println("salary :" + rs.getInt("Emp_salary"));

		}
		con.close();
		System.out.println("Connection closed");

	}

}
```


## Output:
![Screenshot 2023-10-22 171129](https://github.com/Lakshmipriya2005/DBMS/assets/115525361/8ff7f7ea-9d1d-436b-b183-5536d74a6a18)


## Result:
Thust the database is connected and data displayed sucessfully.
