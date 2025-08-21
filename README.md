# aws-rds-quicksight-visualization
A hands-on project to create a database in Amazon RDS (MySQL), connect it with Amazon QuickSight, and build interactive dashboards. Includes SQL scripts, step-by-step guide, and AWS setup.

Step-by-step project to create a relational database in Amazon RDS, connect with QuickSight, and visualize data using SQL + AWS services.
Visualize Data in Amazon RDS with QuickSight
📌 Project Overview

This project demonstrates how to:

Create a Relational Database in Amazon RDS (MySQL/Aurora)

Insert data using MySQL Workbench

Connect RDS with Amazon QuickSight

Build a visualization/dashboard from the data

Secure connections using IAM roles & Security Groups

The main goal is to learn how databases can be managed with AWS and how QuickSight can be used for visualization.

🛠️ Tools & Services Used

AWS RDS (Relational Database Service)

MySQL Workbench

Amazon QuickSight

AWS IAM (Identity & Access Management)

VPC & Security Groups

🚀 Steps Followed

Created Database in RDS using MySQL (Easy Create option).

Configured Security Groups & Inbound Rules for MySQL Workbench access.

Connected MySQL Workbench to the RDS instance and created schema + tables.

Inserted Data into tables (newhire, department).

Connected QuickSight to RDS instance for visualization.

Created Dashboard in QuickSight using employee & department data.

Enhanced Security by configuring IAM Roles & VPC connections.

Deleted Resources at the end to avoid unnecessary AWS charges.

📊 Sample SQL Queries
-- Create employee table
CREATE TABLE newhire(
  empno INT PRIMARY KEY,
  ename VARCHAR(10),
  job VARCHAR(9),
  manager INT NULL,
  hiredate DATETIME,
  salary NUMERIC(7,2),
  comm NUMERIC(7,2) NULL,
  department INT
);

-- Insert sample employees
INSERT INTO newhire (empno, ename, job, manager, hiredate, salary, comm, department) VALUES
(1, 'JOHNSON', 'ADMIN', 6, '1990-12-17', 18000, NULL, 4),
(2, 'HARDING', 'MANAGER', 9, '1998-02-02', 52000, 300, 3);

-- Create department table
CREATE TABLE department(
  deptno INT NOT NULL,
  dname VARCHAR(14),
  loc VARCHAR(13)
);

-- Insert departments
INSERT INTO department (deptno, dname, loc) VALUES  
(1, 'ACCOUNTING', 'ST LOUIS'),
(2, 'RESEARCH', 'NEW YORK');

📈 Final Output

Amazon QuickSight Dashboard named: RDS New Hire Data

Visualizes employee and department details

🛡️ Cleanup

To avoid AWS charges:

Delete QuickSight datasets, dashboards, and account

Delete RDS instance

Delete Security Groups

Delete IAM roles

📖 What I Learned

Difference between SQL (language) vs MySQL (database system)

How IAM roles & policies secure AWS resources

Importance of Inbound rules in VPC Security Groups

How QuickSight connects with RDS to visualize data

✨ This project gave me hands-on experience in AWS database management and BI visualization.
