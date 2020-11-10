# SQL_challenge
Employee database queries within fictional Pewlett Hackard company

###  The instruction was introduced as followss

It is a beautiful spring day, and it is two weeks since you have been hired as a new data engineer at Pewlett Hackard. Your first major task is a research project on employees of the corporation from the 1980s and 1990s. All that remain of the database of employees from that period are six CSV files.
In this assignment, you will design the tables to hold data in the CSVs, import the CSVs into a SQL database, and answer questions about the data. In other words, you will perform:

    - Data Engineering
    - Data Analysis
    
### After analyzing the logic of the csv files, an ERD was created using http://www.quickdatabasediagrams.com.

The data structure of the database needed to follow logically from the csv file content. An ERD was created to illustrate specify data types, primary keys, foreign keys, and other constraints.

![ERD](https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/QuickDBD-Pewlett_Hackard_ERD.png)

YOu will note that every table has a primary key. For dept_manager and dept_emp composite primary keys were created to ensure no duplicate entries of the folloing pairs of data:

        -- dept_manager has composite key dept_no + emp_no
        -- dept_emp has composite key emp_no + dept_no
 
##### If you prefer a tablular view of the data relationships, Click on the PDF link below

![PDF of ERD](https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/QuickDBD-Pewlett_Hackard.pdf)

### To track the files in this endeavor a 'EmployeeSQL' folder was created. Subfolder 'Data' contains the original csv files given; 'solutions' contains the result files

The tables were created in POSTGRES  leveraging the SQL created in the presvious step. Some smalll changes to the QUickDraw generated code were done to ensure proper table creation especially with the composite keys.
Due to foreign key validations care had to be taken to create the tables in logical order; departments, titles and employees were created first followed by dept_emp, dept_manager and salaries. The  sql can be found at (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/Pewlett_Hackard_postgres.sql)

##### Data Analysis tasks were assigned and solutions developed along with output files as delineated below

-- List the following details of each employee: employee number, last name, first name, sex, and salary. (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/output_1_Emp_salary.csv)
-- List first name, last name, and hire date for employees who were hired in 1986. (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/output_2_hired1986.csv)
-- List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name. (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/output_3_manager_info.csv)
-- List the department of each employee with the following information: employee number, last name, first name, and department name. (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/output_4_employee_info.csv
-- List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B." *There were a suprising number of employees fitting this description!*  (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/output_5_Hercules_B_info.csv)
-- List all employees in the Sales department, including their employee number, last name, first name, and department name. (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/output_6_Sales_Emp_info.csv)
-- List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name. * Notice that this query is very similar to the previous but required searching an OR condition.* (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/output_7_Sales_%26_Development_Emp_info.csv)
-- In descending order, list the frequency count of employee last names, i.e., how many employees share each last name. (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/output_8_count_by_Last_names.csv)


