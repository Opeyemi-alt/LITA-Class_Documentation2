# LITA-Class_Documentation2
This is where SQL projects are documented  while learning Data Analysis with the Incubator Hub

### SQL
---

### Project Title: Employee Database Management System and Salary Database
---
### Objective:

Design and implement a database to manage employee information, including positions and state of origin, and salary data.

### Scope:
---
### Database Design:

1. Create tables for:
    - Employees (Staffid, firstname, secondname, Gender, Date of Birth, HireDate)
    - Salaries (Salary ID, Employee ID, Salary Amount, Date Effective)
    - Positions (Position ID, Job Title, Department)
    - States (State ID, State Name)
    - Employee_State (Employee ID, State ID)
2. Establish relationships between tables (foreign keys)

### Queries and Calculations:

1. Calculate total salary expenditure
2. Determine average salary by department
3. Find employees from a specific state
4. Identify employees with a specific job title
5. Generate a report of employee count by state
---
### Deliverables:

1. SQL script to create database schema
2. SQL queries to perform calculations and generate reports
3. Sample data insertion script
4. Written documentation of database design and queries

### Tools and Software:

- SQL Server Management Studio (SSMS)

### Assumptions and Limitations:

- Data accuracy and completeness- Consistent data formatting
- No significant changes in business operations

### Learning Outcomes:

1. Design and implement a database
2. Write efficient SQL queries
3. Perform calculations and generate reports
4. Understand database relationships and normalization

### Database Schema:
```
CREATE TABLE Employees (
  Staffid VARCHAR(255) not null,
  FirstName VARCHAR(255) not null,
  SecondName VARCHAR(255) not null,
  Gender VARCHAR(10),
  Date_of_Birth DATE
  HireDate DATETIME
  PRIMARY KEY(Staffid),
);

CREATE TABLE Salary (
  Salary_id INT PRIMARY KEY,
  Staffid VARCHAR(255),
  firstname VARCHAR(255),
  lastname VARCHAR(255),
  department VARCHAR(255),
);
```


