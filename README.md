# SQL-Filter-Queries

### Project Description:
 The organization is dedicated to enhancing the security of its system. Ensuring the system’s safety, investigating all potential security issues, and updating employee computers as necessary fall under my purview. The subsequent steps outlined below exemplify my utilization of SQL with filter to execute security related tasks. 

 ##

 ### Retrieve after hours failed login attempts:  
  After business hours post – 1800, a potential security incident arose, necessitating investigation into all failed login attempts during this timeframe. The ensuring code illustrates the method I employed to create a SQL query for filtering failed login attempts occurring after business hours. 
  
  ![image](https://github.com/JPass85/SQL-Filter-Queries/assets/141683007/a779d9b5-a5c7-4cba-84a0-00b0ae1e96cf)

 The screenshot comprises my query in the first part and a segment of the output in the second part. This query is designed to isolate failed login attempts transpiring post – 1800. Initially, I retrieved all data from the log_in_attempts table. Subsequently, employing a Where clause with AND operator, I refined the results to exclusively display login attempts that met two criteria: Occurring after 1800 and resulting in failure. The first condition, login_time > ‘1800’, selects logins attempts after 1800, while the second condition, success = FALSE, isolates failed login attempts. 

 ##

 ### Retrieve login attempts on specific dates: 
  A suspicious event unfolded on 2022-05-09. As part of the investigation, all login activity on both 2022-05-09 and the preceding day requires scrutiny. The ensuing code showcases the SQL query I devised to isolate login attempt on these specific dates. 

![image](https://github.com/JPass85/SQL-Filter-Queries/assets/141683007/969f9fe9-6173-4341-9a01-f9571a731ee3)


The screenshot showcases my query in the first part and aa segment of the output of the second part. This query retraces all login attempts that took place on either 2022-05-09 or 2022-05-08. Initially, I selected all data from the log_in_attempts table. Then, employing a WHERE clause with an OR operator, I filtered the results to display only login attempts occurring on either 2022-05-09 or 2022-05-08.

##

### Retrieve login attempts outside of Mexico:  
 After scrutinizing the organization’s login attempts data, I suspected an anomaly with attempts made outside of Mexico. These attempts warrant investigation. Below is the code illustrating the SQL query I developed to filter login attempts from locations outside of Mexico.  

 ![image](https://github.com/JPass85/SQL-Filter-Queries/assets/141683007/0d95db68-d677-44da-944d-fb22a49e68ee)

 The screenshot displays my query in the first part and a segment of the output in the second part. This query retrieves all login attempts that took place in countries other than Mexico. Initially, I started selecting all data from the log_in_attempts table. Then, I utilized a WHERE clause with NOT to filter out countries other than Mexico. For pattern matching, I employed LIKE with ‘MEX%’ to encompass both ‘MEX’ and ‘MEXICO’, as the dataset may represent Mexico in either form. The ‘%’ symbol serves as a wildcard character, representing any number of unspecified characters when used with LIKE. 

 ##

 ### Retrieve employees in Marketing:  
  My team has tasked me with updating the computers of specific employees within the Marketing Department. To accomplish this, I need to gather information on which employee machines require updates. Below is the code illustrating the SQL query I developed to filter for employee machines belonging to employees in the Marketing Department situated in the East building. 

  ![image](https://github.com/JPass85/SQL-Filter-Queries/assets/141683007/d2ebe127-311e-4e09-babf-0b0db5366fc7)

 The screenshot depicts my query in the first part and a portion of the output in the second part. This query retrieves all employees belonging to the Marketing Department in the East building. Initially, I selected all data from the employee's table. Then, I applied a WHERE clause with an AND operator to filter for employees working in both the Marketing Department and East building. For pattern matching, I utilized LIKE with ‘East%’ to accommodate variations in office representation, as the office column denotes the East building with specific office numbers. The first condition, department = ‘Marketing’, isolates employees in the Marketing Department, while the second condition, office LIKE ‘East%’, identifies employees situated in the East building. 

 ##

 ### Retrieve employees in Finance/Sales:  
  To update machines for employees in the Finance and Sales Department, I need to gather information specifically in these two departments. Below is the SQL query I crafted to filter for employee machines belonging to either the Finance or Sales Department. 

  ![image](https://github.com/JPass85/SQL-Filter-Queries/assets/141683007/991c554c-ec8a-4817-8338-8477d41b4691)

 The screenshot displays my query in the first part and a segment of the output in the second part. This query retrieves all employees in the Finance and Sales Departments. Initially, I selected all data from the employees’ table. Then, I employed a WHERE with OR operator to filter for employees in either Finance or Sales departments. Using the OR operator ensures that all employees in either department are included. The first condition, department = ’Finance’, selects employees from the Finance Department, while the second condition, department = ’Sales’, selects employees from the Sales Department.

 ##

 ### Retrieve all employees not in IT:  
  To facilitate a security update for employees outside the Information Technology department, I must gather information about these employees. Below is the SQL query I constructed to filter for employee machines belonging to employees not in the IT Department.

  ![image](https://github.com/JPass85/SQL-Filter-Queries/assets/141683007/afef864e-44f3-4ae5-93ad-20b04b72356f)

The screenshot showcases my query in the first part and a segment of the output in the second part. This query returns all employees not in the IT Department. Initially, I selected all data from the employee table. Then, I utilized a WHERE clause with NOT to filter for employees not in this department. 

##

### Summary:  
I utilized SQL queries with filters to extract specific information regarding login attempts and employee machines from two distinct tables: log_in_attempts and employees. Employing operators such as AND, OR, and NOT enabled me to refine my searches according to the requirements of each task. Additionally, I utilized the LIKE operator alongside the ‘%’ wildcard to filter for patterns within the data. 
