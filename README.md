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

Due to foreign key validations care had to be taken to create the tables in logical order; departments, titles and employees were created first followed by dept_emp, dept_manager and salaries. The  sql can be found at (https://github.com/SJLimburg/SQL_challenge/blob/main/EmployeeSQL/solutions/Pewlett_Hackard_postgres.sql)
