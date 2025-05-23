## Finals Lab Task 1. MySQL Basics
<!-- task needed to complete and instructions -->
The following are the tasks that need to be implemented using MySQL statements. Make sure to complete them in the order specified:
- ### task 1:
  Create table named `employees` with the following fields:  
  - `employee_id` UNIQUE, INTEGER, AUTO-INCREMENT, PRIMARY KEY
  -  `employee_name` VARCHAR(255) and NOT NULL
  -  `manager_id` INTEGER, FOREIGN KEY referencing `employee_id` in the same table (`employees`)
- ### task 2:
  Create table named `departments` with the following fields:
  - `department_id`  UNIQUE, INTEGER, AUTO-INCREMENT, PRIMARY KEY
  - `department_name` VARCHAR(255), NOT NULL
- ### task 3:
  Create table named `employee_departments` with the following fields:
  - `employee_id` INTEGER, FOREIGN KEY referencing `employee_id` in table (`employees`)
  - `department_id` INTEGER, FOREIGN KEY referencing `department_id` in table (`department`)
- ### task 4
  Create table named `employee_projects` with the following fields:
  - `employee_id` INTEGER, FOREIGN KEY referencing `employee_id` in table (`employees`)
  - `project_name` VARCHAR(255), NOT NULL
- ### task 5
  Create table named `managers` with the following fields:
  - `manager_id` UNIQUE, INTEGER, AUTO-INCREMENT, PRIMARY KEY
  - `employee_id` INTEGER, FOREIGN KEY referencing `employee_id` in table (`employees`)



 <!-- required output-->
## Required output per Test Cases:
1. Query statements (Task 1-5)
2. Table Structure (Task 1-5)
3. And 1 ER Diagram or Relational schema from phpMyAdmin or Workbench (pdf or jpg file)
4. Sql copy of the database and table sturctures


<!-- step by step -->
## STEP 1:
- Open XAMPP and start the Apatche and MySQL then open MySQL workbench
- Add a new connection
- Click the connection made
## STEP 2:
- Create a DATABASE BY using  
 `CREATE DATABE database_name`
- Use the database that has created by using  
  `USE database_name`

  <!-- screenshots and code  -->
## HERE IS THE SCREENSHOT OF TASK 1 TO TASK 4
### task 1
![](image/FTASK1.1.png)  
- code  
  `CREATE TABLE employees_tbl (employee_id INT(3) UNIQUE AUTO_INCREMENT PRIMARY KEY,
 employee_name VARCHAR(255) NOT NULL,
 manager_id INT(3), FOREIGN KEY(manager_id) REFERENCES employees_tbl(employee_id));`
### task 2
![](image/FTASK1%2C2.png)
- code  
  `CREATE TABLE departments_tbl (department_id INT(3) UNIQUE AUTO_INCREMENT PRIMARY KEY,
 department_name VARCHAR(255) NOT NULL);`
### task 3
![](image/FTASK1.3.png)
- code  
`CREATE TABLE employee_departments_tbl (employee_id INT(3), FOREIGN KEY (employee_id) REFERENCES employees_tbl(employee_id),
department_id INT(3), FOREIGN KEY(department_id) REFERENCES departments_tbl(department_id));`
### task 4
![](image/FTASK1.4.png)
- code  
  `CREATE TABLE employee_projects_tbl (employee_id INT(3), FOREIGN KEY(employee_id) REFERENCES employees_tbl(employee_id),
 project_name VARCHAR(255) NOT NULL);`
### task 5
![](image/FTASK1.5.png)
- code  
  `CREATE TABLE managers_tbl (manager_id INT(3) UNIQUE AUTO_INCREMENT PRIMARY KEY,
employee_id INT(3), FOREIGN KEY(employee_id) REFERENCES employees_tbl(employee_id));`


<!-- ER Diagram -->
## HERE IS THE SCREENSHOT OF ER DIAGRAM
![](image/FTASK1.6.png)

<!--SQL FILES-->
## HERE IS MY SQL FILE
[employees Table](file/multi_level_company_employee_projects.sql)  
[departments Table](file/multi_level_company_employee_departments.sql)  
[employee departments Table](file/multi_level_company_employee_departments.sql)  
[employee projects Table](file/multi_level_company_employee_projects.sql)  
[managers Table](file/multi_level_company_managers.sql)  
