-- Creating the tables with only primary keys in the order of which the csv lists each field.

--Begin Statement for creating tables with primary keys and altering tables to incorporate foreign keys.
BEGIN;

-- Creating the employee table with a primary key

CREATE TABLE IF NOT EXISTS public.employees
(
    emp_no character varying(30) NOT NULL,
	emp_title_id character varying(30),
	birth_date character varying(30),
	first_name character varying(255),
	last_name character varying(255),
	sex character varying(30),
    hire_date character varying(30),
    PRIMARY KEY (emp_no)
);

-- Creating a titles table with a primary key
CREATE TABLE IF NOT EXISTS public.titles
(
    title_id character varying(30) NOT NULL,
    title character varying(255),
    PRIMARY KEY (title_id)
);

-- Creating a salaries table with no primary key.
CREATE TABLE IF NOT EXISTS public.salaries
(
    emp_no character varying(30) NOT NULL,
    salary integer
);

-- Creating a dept_emp table with no primary key.
CREATE TABLE IF NOT EXISTS public.dept_emp
(
    emp_no character varying(30) NOT NULL,
    dept_no character varying(30)
);

-- Creating a dept_manager with no primary key.
CREATE TABLE IF NOT EXISTS public.dept_manager
(
    dept_no character varying(30) NOT NULL,
    emp_no character varying(30)
);

-- Creating a departments table with no primary key.
CREATE TABLE IF NOT EXISTS public.departments
(
    dept_no character varying(30) NOT NULL,
    dept_name character varying(255) NOT NULL,
    PRIMARY KEY (dept_no)
);

-- Incorporating foreign key into the dept_manager table.  
ALTER TABLE public.dept_manager
    ADD FOREIGN KEY (dept_no)
    REFERENCES public.departments (dept_no)
    NOT VALID;

-- Incorporating foreign key into the dept_manager table.  
ALTER TABLE public.dept_manager
    ADD FOREIGN KEY (emp_no)
    REFERENCES public.employees (emp_no)
    NOT VALID;

-- Incorporating foreign key into the employees table.  
ALTER TABLE public.employees
    ADD FOREIGN KEY (emp_title_id)
    REFERENCES public.titles (title_id)
    NOT VALID;

-- Incorporating foreign key into the salaries table.  
ALTER TABLE public.salaries
    ADD FOREIGN KEY (emp_no)
    REFERENCES public.employees (emp_no)
    NOT VALID;

-- Incorporating foreign key into the dept_emp table.  
ALTER TABLE public.dept_emp
    ADD FOREIGN KEY (emp_no)
    REFERENCES public.employees (emp_no)
    NOT VALID;

-- Incorporating foreign key into the dept_emp table.  
ALTER TABLE public.dept_emp
    ADD FOREIGN KEY (dept_no)
    REFERENCES public.departments (dept_no)
    NOT VALID;

--End Statement for all table creation and altering.
END;

-- Incorporate date format into hire date and birth date.
ALTER TABLE employees 
ALTER COLUMN birth_date 
TYPE DATE 
USING (birth_date::date);

ALTER TABLE employees 
ALTER COLUMN hire_date 
TYPE DATE 
USING (hire_date::date);
