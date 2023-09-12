# DataBaseFirstEFCoreMVC
This is simple application demonstrating Entity Framework Database First approach in .NET 7.0

Follow the below steps to get this project working for you.

Step 1. Create below Tables in SQL Server and insert data 

Create Students table and insert sample data
   ```
   CREATE TABLE Students (
    StudentID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Gender VARCHAR(10),
    DateOfBirth DATE,
    Major VARCHAR(50),
    GPA DECIMAL(3, 2)
);
```
This SQL code defines a table named "Students" with columns for StudentID, FirstName, LastName, Gender, DateOfBirth, Major, and GPA.

Now, let's insert some sample data into the table:

INSERT INTO Students (StudentID, FirstName, LastName, Gender, DateOfBirth, Major, GPA)
VALUES
    (1, 'John', 'Doe', 'Male', '1995-02-15', 'Computer Science', 3.5),
    (2, 'Jane', 'Smith', 'Female', '1998-07-20', 'Biology', 3.2),
    (3, 'Alice', 'Johnson', 'Female', '1997-11-10', 'History', 3.8),
    (4, 'Bob', 'Brown', 'Male', '1996-05-03', 'Mathematics', 3.9),
    (5, 'Emily', 'Davis', 'Female', '1999-03-25', 'Psychology', 3.4);
This SQL code inserts five sample student records into the "Students" table. Each record includes a unique StudentID, FirstName, LastName, Gender, DateOfBirth, Major, and GPA.

Create Employee table and insert sample data

```
CREATE TABLE Employee (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Email VARCHAR(100),
    HireDate DATE,
    Department VARCHAR(50),
    Salary DECIMAL(10, 2)
);
```
This SQL code defines a table named "Employee" with columns for EmployeeID, FirstName, LastName, Email, HireDate, Department, and Salary.

Now, let's insert some sample data into the table:

INSERT INTO Employee (EmployeeID, FirstName, LastName, Email, HireDate, Department, Salary)
VALUES
    (1, 'John', 'Doe', 'john.doe@example.com', '2020-01-15', 'IT', 60000.00),
    (2, 'Jane', 'Smith', 'jane.smith@example.com', '2019-05-20', 'HR', 55000.00),
    (3, 'Alice', 'Johnson', 'alice.johnson@example.com', '2021-03-10', 'Finance', 65000.00),
    (4, 'Bob', 'Brown', 'bob.brown@example.com', '2018-09-03', 'Marketing', 58000.00),
    (5, 'Emily', 'Davis', 'emily.davis@example.com', '2022-02-25', 'IT', 62000.00);
This SQL code inserts five sample employee records into the "Employee" table. Each record includes a unique EmployeeID, FirstName, LastName, Email, HireDate, Department, and Salary.

Step 2. Clone the repository

Step 3. Execute below command for Scaffold DbContext

Scaffold-DbContext ""Name=ConnectionStrings:DataBaseConnectionString";" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models

Step 4. build and run the project
