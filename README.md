## 🚀 Data Transformer — Advanced SQL Project



## 📌 About The Project

Data Transformer is a practical SQL project designed to demonstrate advanced SQL concepts used in real-world data analysis and reporting.

The project simulates a Corporate Data Analysis System containing customer information, sales transactions, and employee performance data.

It focuses on transforming raw data into meaningful information using:

- 🔗 SQL Joins
- 🧩 Subqueries
- 📅 Date & Time Functions
- 🔤 String Functions
- 📊 Window Functions
- 🏆 Ranking Functions
- 🧮 Aggregate Functions
- 🔀 CASE Expressions
- 🧹 Data Cleaning & Transformation

---

## 🎯 Project Objective

The main objective of this project is to strengthen practical knowledge of advanced SQL operations and learn how to manipulate and transform data for:

- Business reporting
- Data analysis
- Data cleaning
- Customer analysis
- Sales analysis
- Employee performance analysis
- Complex SQL queries

---

## 🏢 Project Overview

The project contains three major areas:

👥 1. Customer Information Management

Stores and manages customer-related information such as:

- Customer ID
- First Name
- Last Name
- Email
- Registration Date

🛒 2. Sales Transaction Processing

Stores customer orders and transaction information including:

- Order ID
- Customer ID
- Order Date
- Total Amount

👨‍💼 3. Employee Performance Data

Stores employee information including:

- Employee ID
- First Name
- Last Name
- Department
- Hire Date
- Salary

---

🗄️ Database Structure

                 ┌─────────────────────┐
                 │      Customers      │
                 ├─────────────────────┤
                 │ PK CustomerID       │
                 │ FirstName           │
                 │ LastName            │
                 │ Email               │
                 │ RegistrationDate    │
                 └──────────┬──────────┘
                            │
                            │ CustomerID
                            │
                 ┌──────────▼──────────┐
                 │       Orders        │
                 ├─────────────────────┤
                 │ PK OrderID          │
                 │ FK CustomerID       │
                 │ OrderDate           │
                 │ TotalAmount         │
                 └─────────────────────┘


                 ┌─────────────────────┐
                 │     Employees       │
                 ├─────────────────────┤
                 │ PK EmployeeID       │
                 │ FirstName           │
                 │ LastName            │
                 │ Department          │
                 │ HireDate            │
                 │ Salary              │
                 └─────────────────────┘

---

## 🧰 Technologies Used

Technology

| Purpose
MySQL 8.0
| Database Management
SQL


| Data Manipulation & Analysis

GitHub Version Control & Project Hosting
MySQL Workbench|

Query Execution & Database Development

---

## 📋 SQL Tasks Performed

This project contains 17 practical SQL tasks.

🔗 Joins

1. INNER JOIN
   Retrieve orders along with matching customer details.

2. LEFT JOIN
   Retrieve all customers and their corresponding orders.

3. RIGHT JOIN
   Retrieve all orders and their corresponding customers.

4. FULL OUTER JOIN
   Retrieve all customers and orders regardless of matching records.

«Note: MySQL does not directly support "FULL OUTER JOIN", so a combination of "LEFT JOIN", "RIGHT JOIN", and "UNION" is used.»

---

🧩 Subqueries

5. Find customers who placed orders above the average order amount.

6. Find employees whose salaries are above the average salary.

---

📅 Date Functions

7. Extract the year and month from "OrderDate".

8. Calculate the number of days between "OrderDate" and the current date.

9. Format the order date into a readable format such as:

01-Jul-2023

---

🔤 String Functions

10. Concatenate "FirstName" and "LastName" into a full name.

11. Replace part of a string using "REPLACE()".

12. Convert:

FirstName → UPPERCASE
LastName  → lowercase

13. Remove unnecessary spaces from email addresses using "TRIM()".

---

📊 Window Functions

14. Calculate the running total of order amounts.

15. Rank orders according to "TotalAmount" using "RANK()".

---

🔀 CASE Expressions

16. Assign discounts based on order amount:

Order Amount| Discount
> 1000| 10%
> 500| 5%
≤ 500| 0%

17. Categorize employee salaries as:

Salary| Category
≥ 80,000| High
≥ 60,000| Medium
< 60,000| Low

---

🧠 SQL Concepts Demonstrated

JOIN
├── INNER JOIN
├── LEFT JOIN
├── RIGHT JOIN
└── FULL OUTER JOIN concept


SUBQUERIES
├── AVG()
└── Nested SELECT


DATE FUNCTIONS
├── YEAR()
├── MONTH()
├── MONTHNAME()
├── DATEDIFF()
└── DATE_FORMAT()


STRING FUNCTIONS
├── CONCAT()
├── REPLACE()
├── UPPER()
├── LOWER()
└── TRIM()


WINDOW FUNCTIONS
├── SUM() OVER()
└── RANK() OVER()


CONDITIONAL LOGIC
└── CASE WHEN

---

▶️ How To Run This Project

1️⃣ Clone the Repository

git clone https://github.com/your-username/data-transformer.git

2️⃣ Open MySQL Workbench

Open MySQL Workbench or another MySQL-compatible SQL environment.

3️⃣ Create the Database

Run:

SOURCE SQL/database.sql;

Or execute the "database.sql" file manually.

4️⃣ Create Tables

Run:

SQL/tables.sql

5️⃣ Insert Sample Data

Run:

SQL/sample_data.sql

6️⃣ Execute Queries

Open:

SQL/queries.sql

Run the queries individually and verify the results.

---

## 📊 Sample Data

Customers

CustomerID| FirstName| LastName| Email

1| rskesh| pedduri| rakesh.pedduri@gmail.com 

2| yash| pandey| yash.pandey@gmail.com 

3| kalpesh| patil|  kalpesh.patil@gmail.com

4| kunal| rajput| kunal.rajuput@gmail.com

5| jiya| patel| jiya.patel@gmail.com


Orders


OrderID| CustomerID| OrderDate| TotalAmount

101| 1| 2023-07-01| 150.50

102| 2| 2023-07-03| 200.75

103| 1| 2023-07-10| 750.00

104| 3| 2023-08-15| 1200.00

105| 4| 2023-09-01| 450.25

106| 2| 2023-09-15| 650.00

107| 3| 2023-10-05| 1100.00


---

## 💡 Key Learning Outcomes

By completing this project, the following SQL skills are demonstrated:

- Understanding relationships between tables
- Performing different types of joins
- Writing nested subqueries
- Working with dates
- Cleaning and transforming text data
- Using aggregate functions
- Using window functions
- Applying ranking logic
- Creating conditional business rules
- Preparing data for reporting and analysis

---

## 📝 Assumptions

The following assumptions were made where the requirements did not specify exact values:

1. Salary Classification

Salary >= 80,000 → High
Salary >= 60,000 → Medium
Salary < 60,000  → Low

2. Discount Rules

Amount > 1000 → 10%
Amount > 500  → 5%
Amount <= 500 → 0%

3. The project uses MySQL 8.0 syntax.

4. Since MySQL does not provide direct "FULL OUTER JOIN" syntax, "LEFT JOIN + RIGHT JOIN + UNION" is used.

---

## 🔐 Data Integrity

The project uses:

- Primary Keys
- Foreign Keys
- Appropriate data types
- Relational table design

Relationship:

Customers.CustomerID
        │
        │ 1 : Many
        ▼
Orders.CustomerID

One customer can have multiple orders.

---

## 📚 Documentation

Detailed project documentation is available here:

Documentation/project_documentation.md

The documentation contains:

- Project overview
- Database structure
- Table descriptions
- SQL concepts
- Query explanations
- Assumptions
- Expected outcomes

---

## 🚀 Future Improvements

The project can be extended with:

- 📊 Sales dashboards
- 📈 Monthly revenue analysis
- 👥 Customer segmentation
- 🏆 Top customer analysis
- 💰 Revenue forecasting
- 📦 Product-level sales analysis
- 📅 Monthly and yearly reports
- 🔍 Advanced analytical queries

---

## 👨‍💻 Author

RAKESH PEDDURI

«SQL | Data Analysis | MySQL»

---

## ⭐ Project Status

Completed ✅

This project was created as a practical SQL assignment to demonstrate advanced SQL concepts and data transformation techniques.

---

<p align="center">⭐ If you found this project useful, consider giving it a star!

Made with 💙 using SQL & MySQL

</p>
