# SQL_IMPLEMENTATION FOR EMPLOYEE DETAILS:

````
-- Create database
CREATE DATABASE EmployeeDB;

-- Use the database
USE EmployeeDB;

-- Create Employee Details table
CREATE TABLE Details (
    Employee_Id VARCHAR(100),
    Employee_name VARCHAR(100),
    dateofBirth DATE,
    DateOfjoining DATE,
    Salary INT,
    Bonus INT,
    City VARCHAR(100),
    Address VARCHAR(100),
    Department VARCHAR(100),
    Employee_mail_id VARCHAR(100),
    Employee_status VARCHAR(100),
    Timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    Phone_number VARCHAR(10)
);

-- Display the table structure
DESC Details;

-- Insert values into the table
INSERT INTO Details (Employee_Id, Employee_name, dateofBirth, DateOfjoining, Salary, Bonus, City, Address, Department, Employee_mail_id, Employee_status, Phone_number)
VALUES
('ds001', 'Sharanya', '1985-05-15', '2010-08-23', 70000, 5000, 'Delhi', '1234 Rajpath Rd', 'HR', 'sha2005ranya@gmail.com', 'Active', '9876543210'),
('ds002', 'Sujitha', '1990-03-12', '2015-07-30', 75000, 6000, 'Mumbai', '5678 Bandra East', 'Finance', 'suji@gmail.com', 'Active', '9123456789'),
('ds003', 'Parkavi', '1982-11-22', '2008-05-10', 80000, 7000, 'Bangalore', '9101 MG Road', 'IT', 'paru@gmail.com', 'Inactive', '9345678901'),
('ds004', 'Janani', '1995-02-05', '2018-01-25', 68000, 4000, 'Chennai', '1234 Anna Nagar', 'Marketing', 'janani@gmail.com', 'Active', '9786541230'),
('ds005', 'Shiva Dharani', '1980-07-09', '2005-03-13', 95000, 8000, 'Hyderabad', '6789 Banjara Hills', 'Operations', 'svdharani@gmail.com', 'Active', '9345678123'),
('ds006', 'Nanthini', '1993-10-16', '2017-11-05', 72000, 5500, 'Pune', '2345 Koregaon Park', 'Legal', 'Nanthini@gmail.com', 'Active', '9876123456'),
('ds007', 'Navanithi', '1988-04-23', '2014-02-11', 85000, 6500, 'Kolkata', '3456 Salt Lake City', 'Engineering', 'navanithi@gmail.com', 'Inactive', '9912345678'),
('ds008', 'Aashif Shadin', '1997-08-30', '2020-06-19', 60000, 3000, 'Jaipur', '4567 C-Scheme', 'Sales', 'aashi@gmail.com', 'Active', '9034567890'),
('ds009', 'Santhosh', '1984-01-10', '2009-09-07', 77000, 5200, 'Lucknow', '5678 Hazratganj', 'Support', 'sandy@gmail.com', 'Active', '9123987456'),
('ds010', 'Praveen', '1992-12-20', '2016-10-17', 73000, 4800, 'Ahmedabad', '6789 Navrangpura', 'Finance', 'bheem@gmail.com', 'Active', '9384765120');

-- Change column name from Employee_name to First_name
ALTER TABLE Details
CHANGE COLUMN Employee_name First_name VARCHAR(100);

-- Add new column Age
ALTER TABLE Details
ADD COLUMN Age INT;

-- Update Age based on date of birth
UPDATE Details
SET Age = TIMESTAMPDIFF(YEAR, dateofBirth, CURDATE());

-- Drop Employee_status column
ALTER TABLE Details
DROP COLUMN Employee_status;

-- Delete a record
DELETE FROM Details WHERE Employee_Id = 'ds006';

-- Queries:

-- Display names ending with 'a'
SELECT * FROM Details WHERE First_name LIKE '%a';

-- Employees with salary more than 70,000
SELECT * FROM Details WHERE Salary > 70000;

-- Employees from Chennai
SELECT * FROM Details WHERE City = 'Chennai';

-- Employees aged 19 in the Finance department
SELECT * FROM Details WHERE Age = 19 AND Department = 'Finance';

-- Count of employees with salary more than 90,000
SELECT COUNT(*) FROM Details WHERE Salary > 90000;

-- Average age in Finance department
SELECT AVG(Age) FROM Details WHERE Department = 'Finance';

-- Maximum and Minimum Salary
SELECT MAX(Salary) AS Highest_Salary FROM Details;
SELECT MIN(Salary) AS Lowest_Salary FROM Details;

-- Employees whose name starts with 'A'
SELECT * FROM Details WHERE First_name LIKE 'A%';

-- Employees with 'A' in the middle of their name and salary between 85,000 and 90,000
SELECT * FROM Details WHERE First_name LIKE '%a%' AND Salary BETWEEN 85000 AND 90000;

-- Truncate the table (Deletes all records but keeps structure)
TRUNCATE TABLE Details;


``````````
