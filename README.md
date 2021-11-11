## Background

I was asked to analyze a set of six csvs from a hypothetical company that includes the following:

   1. 'titles'
   2. 'employees'
   3. 'dept_manager'
   4. 'dept_emp'
   5. 'salaries'
   6. 'departments' 

This hypothetical company has two decades worth of employee data, both current and past employees.  The following tasks were done using Postgres:

   1. Developed an ERD diagram identifying all of the columns, their object types, and primary and foreign keys for each of the tables that corresponded to each csv.
   2. Code was developed to generate the tables, first starting on the creation of the tables and only their primary keys followed by a set of queries altering tables and columns to associate the foreign keys and change the object type to a date format.
   3. Imported the table data using the Postgres GUI.
   4. Conducted an analysis of the data answering eight questions.

Regarding the latter item, the questions included the following:

   1. List the following details of each employee: employee number, last name, first name, sex, and salary.
   2. List first name, last name, and hire date for employees who were hired in 1986.
   3. List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.
   4. List the department of each employee with the following information: employee number, last name, first name, and department name.
   5. List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."
   6. List all employees in the Sales department, including their employee number, last name, first name, and department name.
   7. List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.
   8. In descending order, list the frequency count of employee last names, i.e., how many employees share each last name.

This repository includes the following:

   1. 'EmployeeSQL' folder containing the original csvs
   2. 'Postgres_files' folder containing the Postgres generated queries as saved through the GUI.
   3. 'sql_files' folder containing the two queries used; one that generates the table schemata and another that contains the queries to answer the eight questions listed above.
   4. 'erd.png' file that provides a visual of what the ERD looks like.

All of the data contained in this repository could be useful and applied to real life situations where salary or demographic information may need to be analyzed across a large company.  