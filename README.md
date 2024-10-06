# InNeeD Online Academy - Database Development

This repository contains the MySQL database implementation for *InNeeD Online Academy*, an e-learning platform that serves learners across 8 branches in the UK. The database supports key functionalities like course enrollment, payment processing, role-based access control, and certificate issuance.

## Project Overview

InNeeD Online Academy is a platform providing flexible and accessible e-learning opportunities. This project involved the design and development of a MySQL database to manage users, courses, payments, and evaluations. The system supports multiple user roles such as students, employees, trainers, and the CEO, each with specific functionalities.

### Key Features
- *Role-Based Access Control*: Secure access for customers, trainers, employees, branch managers, and the CEO.
- *Automated Workflows*: Enrollment verification, payment tracking, and certificate issuance.
- *Stored Procedures*: Efficient CRUD operations for managing users, courses, payments, and evaluations.
- *AWS Deployment*: The database is hosted on AWS for scalability and secure remote access.

## Database Structure

The database consists of several tables designed for various entities including:
- *Customers*
- *Courses*
- *Employees*
- *Trainers*
- *Transactions*
- *Enrollments*
- *Evaluations*

Each table is structured with appropriate data types and relationships to ensure referential integrity.

### ER Diagram
Include the ER diagram image (optional):
[here](https://drive.google.com/file/d/1N7VChcDTE3Bk9tD6eV7uLgjIjUpjNB-1/view?usp=sharing).

### SQL Features
- *Stored Procedures*: Over 15 stored procedures for operations like course enrollment, payment verification, and profile updates.
- *Triggers and Constraints*: To maintain data integrity and ensure that business rules are enforced (e.g., checking prerequisites for courses).
- *Automated Certificate Generation*: Certificates are automatically generated upon course completion based on evaluations.

## Installation and Usage

### Prerequisites
- *MySQL* installed on your local machine or an AWS RDS instance.
- *MySQL Workbench* (optional but recommended for visualization and management).

### Setup

1. *Clone the repository*:
   bash
   git clone https://github.com/prashantkr2805/InNEED-Database-Development.git
   

2. *Create the Database*:
   - Open MySQL Workbench or any other MySQL client.
   - Run the SQL script located in the /sql-scripts folder to set up the database schema:
     [here](https://docs.google.com/document/d/1Yn_Vl_DnlwEwZ0mUWsEZAAhLHxsDNfIr/edit?usp=sharing&ouid=117613726400409974751&rtpof=true&sd=true).

3. *Stored Procedures*:
   - After setting up the schema, execute the stored procedures for operations like Sign_Up, BuyNow, and enrollstudent.

4. *AWS Access*:
   - The database can also be hosted on *AWS RDS*. Use the following credentials to connect (replace with your credentials):
     - Host: http://your-rds-endpoint
     - Username: admin
     - Password: yourpassword
   
   Access and modify the data using *MySQL Workbench* or any SQL client.

### Example Usage
- *Customer Registration*:
   sql
   CALL Sign_Up('John', 'Doe', '1234AB', 'john.doe@example.com', '0771234567', 'Graduate', 'password123', 'London');
   
- *Course Enrollment*:
   sql
   CALL enrollstudent('2023-11-12', '300145', '7');
   
- *Payment Processing*:
   sql
   CALL BuyNow('56432', '2023-08-11', '200', '300145');
   

## Documentation
For more details, refer to the [project report](https://drive.google.com/file/d/1QasXwffBrnm85-mFZjW6gidx9GCDBP7S/view?usp=drive_link).

## Technologies Used
- *MySQL* for database management.
- *AWS RDS* for database hosting.
- *MySQL Workbench* for database modeling and querying.

## Contact
For any inquiries or collaboration, feel free to reach out to me via LinkedIn(https://www.linkedin.com/in/prashant-kumar-b525a3219/).
