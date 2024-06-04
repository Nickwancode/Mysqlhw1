# Mysqlhw1
SELECT Id as EmployeeID, Name, Department, City, Title as Project, ClientId
FROM Employee 
INNER JOIN Projects 
ON Employee.Id = Projects.EmployeeId;
Specifically, an inner join returns only the rows that have matching values in both tables being joined. All non matching rows are gone. and join does the same thing.
SELECT Id as EmployeeID, Name, Department, City, Title as Project, ClientId
FROM Employee 
LEFT OUTER JOIN Projects 
ON Employee.Id = Projects.EmployeeId;
returns all the rows from the left table (the table specified before the JOIN keyword) and the matched rows from the right table (the table specified after the JOIN keyword). If there are no matching rows in the right table, the result set will contain NULL values for columns from the right table.

SELECT Employee.Id as EmployeeId, Name, Department, City, Title as Project
FROM Employee 
RIGHT OUTER JOIN Projects 
ON Employee.Id = Projects.EmployeeId;

A right outer join in MySQL, also known as simply a right join, is used to combine data from two tables while ensuring all rows from the right-hand table are included.

SELECT Employee.Id as EmployeeId, Name, Department, City, Title as Project 
FROM Employee 
LEFT OUTER JOIN Projects 
ON Employee.Id = Projects.EmployeeId
UNION 
SELECT Employee.Id as EmployeeId, Name, Department, City, Title as Project 
FROM Employee 
RIGHT OUTER JOIN Projects 
ON Employee.Id = Projects.EmployeeId;
**union operator is used to combine the results of two or more SELECT statements into a single result set. It removes duplicate rows by default.
SELECT Employee.Id as EmployeeId, Name, Department, City, Title as Project
FROM Employee 
CROSS JOIN Projects;
Cross join It creates a new row for every possible combination of a row from the first table with a row from the second table.
