# SQL Challenge: Employee Database Analysis  

## Background  

As a newly hired data engineer at **Pewlett Hackard**, you’ve been tasked with reconstructing and analyzing the company’s employee database from the 1980s and 1990s. This involves designing a relational database schema, importing historical CSV data, and performing detailed SQL queries to answer key questions about the organization’s workforce.  

---

## Repository Structure  

The repository is organized as follows:  

```  
sql-challenge/  
│  
├── EmployeeSQL/  
│   ├── Data/                     # Folder containing the six CSV files  
│   │   ├── employees.csv  
│   │   ├── departments.csv  
│   │   ├── titles.csv  
│   │   ├── salaries.csv  
│   │   ├── dept_emp.csv  
│   │   └── dept_manager.csv  
│   │  
│   ├── schema.sql                # SQL script to create the database schema  
│   ├── import_data.sql           # SQL script to import CSV data into tables  
│   ├── analysis_queries.sql      # SQL script containing all data analysis queries  
│   ├── ERD.png                   # Entity Relationship Diagram for the database  
│   └── README.md                 # This README file  
│  
└── .gitignore                    # File to exclude unnecessary files (e.g., CSVs)  
```  

---

## Objectives  

The project is divided into three main parts:  

### 1. Data Modeling  

- **Goal**: Design an Entity Relationship Diagram (ERD) to map out the relationships between the six CSV files.  
- **Steps**:  
  - Inspect the CSV files to identify fields, data types, and relationships.  
  - Use a tool like **QuickDBD** or another ERD generator to create a detailed diagram.  
  - Identify primary keys, foreign keys, and constraints for each table.  

### 2. Data Engineering  

- **Goal**: Create a database schema and import the CSV data into SQL tables.  
- **Steps**:  
  1. Write a **schema.sql** file to define the structure of each table, including:  
     - Data types  
     - Primary and foreign keys  
     - Constraints (e.g., `NOT NULL`)  
  2. Ensure the tables are created in an order that respects foreign key dependencies.  
  3. Use the **import_data.sql** file to import the six CSV files into the respective tables.  

### 3. Data Analysis  

- **Goal**: Answer specific business questions using SQL queries.  
- **Steps**:  
  - Write SQL queries for the following tasks:  
    1. List the employee number, last name, first name, sex, and salary of each employee.  
    2. Identify employees hired in 1986 (include first name, last name, and hire date).  
    3. List managers of each department along with their department info.  
    4. Show department information (number, name) for each employee.  
    5. Find employees whose first name is **Hercules** and last name starts with "B".  
    6. List employees in the **Sales** department.  
    7. List employees in both **Sales** and **Development** departments.  
    8. Show frequency counts of employee last names in descending order.  

---

## Installation  

### Prerequisites  

1. Install a relational database management system (e.g., PostgreSQL, MySQL, or SQLite).  
2. Install a SQL client (e.g., pgAdmin, MySQL Workbench, or DBeaver).  

### Setup Instructions  

1. **Clone the Repository**  
   ```bash  
   git clone https://github.com/your-username/sql-challenge.git  
   cd sql-challenge/EmployeeSQL  
   ```  

2. **Create the Database**  
   - Open your SQL client and execute the **schema.sql** script to create the database structure:  
     ```sql  
     \i schema.sql  
     ```  

3. **Import Data**  
   - Execute the **import_data.sql** script to populate the tables with data from the CSV files:  
     ```sql  
     \i import_data.sql  
     ```  

4. **Run Analysis Queries**  
   - Open and execute the **analysis_queries.sql** file to run the queries for data analysis.  

---

## Entity Relationship Diagram  

The following diagram represents the database schema and relationships:  

![Entity Relationship Diagram](ERD.png)  

---

## Key Findings  

### 1. Employee Data  
- Total number of employees analyzed: X (calculated from the `employees` table).  

### 2. Hiring Patterns  
- Number of employees hired in 1986: X  
- Most common hiring year: X  

### 3. Manager-Department Analysis  
- Total number of managers: X  
- Department with the highest number of employees: X  

### 4. Name Frequency Analysis  
- The most common last name among employees is **X**, shared by **Y** employees.  
