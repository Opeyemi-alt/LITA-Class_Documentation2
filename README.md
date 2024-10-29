# LITA-Class_Documentation2
This is where SQL projects are documented  while learning Data Analysis with the Incubator Hub

### SQL
---

### Project Title: Employee Database Management System and Salary Database

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

### Deliverables:
---
1. SQL script to create database schema
2. SQL queries to perform calculations and generate reports
3. Sample data insertion script
4. Written documentation of database design and queries

### Tools and Software:
---
- SQL Server Management Studio (SSMS)

### Assumptions and Limitations:
---
- Data accuracy and completeness- Consistent data formatting
- No significant changes in business operations

### Learning Outcomes:
---

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
Sample Queries:

1. Calculate total salary expenditure:

SELECT SUM(Salary_Amount) FROM Salaries;

1. Determine average salary by department:


```SELECT Department, AVG(Salary_Amount) 
FROM Positions 
JOIN Salaries ON Positions.PositionID = Salaries.EmployeeID 
GROUP BY Department;
```

1. Find employees from a specific state:
   
```
SELECT * 
FROM Employees 
JOIN Employee_State ON Employees.EmployeeID = Employee_State.EmployeeID 
JOIN States ON Employee_State.StateID = States.StateID 
WHERE States.State_Name = 'New York';
```

### Data Visualization

![WhatsApp Image 2024-10-29 at 15 20 59_e81b35e8](https://github.com/user-attachments/assets/36bde8f1-4ab3-4ed6-a3eb-e4525b272af3)


![WhatsApp Image 2024-10-29 at 15 21 16_9253022f](https://github.com/user-attachments/assets/b3099c55-504d-410d-af27-5d5da01b71c3)

