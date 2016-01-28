# Description: SQL Queries for Employees Database

####001. Display all databases in any MySQL instance.
```sql
show databases;
```

####002. Switch to EMPLOYEES database.
```sql
use employees;
```

####003. Display all tables in the EMPLOYEES database.
```sql
show tables;
```

####004. Display the schema of EMPLOYEES table in the EMPLOYEES database.
```sql
describe employees;
```

####005. Display all the information from the EMPLOYEES table.
```sql
select * from employees;
```

####006. Find the total number of records in the EMPLOYEES table.
```sql
select count(*) from employees;
```

####007. Display any 10 records from the EMPLOYEES table.
```sql
select * from employees limit 10;
```

####008. Display EMP_NO, FIRST_NAME, LAST_NAME and GENDER from the EMPLOYEES table.
```sql
select emp_no, first_name, last_name, gender from employees;
```

####009. Display EMP_NO, FIRST_NAME, LAST_NAME and GENDER from the EMPLOYEES table sorted by FIRST_NAME.
```sql
select emp_no, first_name, last_name, gender from employees order by first_name;
```

####010. Display EMP_NO, FIRST_NAME, LAST_NAME and GENDER from the EMPLOYEES table sorted by LAST_NAME in descending order.
```sql
select emp_no, first_name, last_name, gender from employees order by last_name desc;
```

####011. Display EMP_NO, FIRST_NAME, LAST_NAME and GENDER from the EMPLOYEES table sorted by LAST_NAME in descending order and FIRST_NAME in ascending order.
```sql
select emp_no, first_name, last_name, gender from employees order by last_name desc, first_name asc;
```

####012. Display EMP_NO, FIRST_NAME, LAST_NAME and GENDER from the EMPLOYEES table sorted by LAST_NAME in descending order and FIRST_NAME in ascending order. Limit the result set to just 20 records.
```sql
select emp_no, first_name, last_name, gender from employees order by last_name desc, first_name asc limit 20;
```

####013. Find all those employees whose FIRST_NAME is 'Bikash'.
```sql
select * from employees where first_name = 'Bikash';
```

####014. Find all those employees whose FIRST_NAME starts with the letter 'B'.
```sql
select * from employees where first_name like 'B%';
```

####015. Find the total number of employees whose FIRST_NAME is 'Bikash'.
```sql
select count(*) from employees where first_name = 'Bikash';
```

####016. Find the total number of male and female employees.
```sql
select count(*), gender from employees group by gender;
```

####016. Display all unique FIRST_NAME from the EMPLOYEES table.
```sql
select distinct first_name from employees;
```

####017. Find all those employees who joined before 1986.
```sql
select * from employees where hire_date < '1986-01-01';
```

####018. Find all those employees who joined during last 3 days of 1986. Display the result in ascending order of their hiring date.
```sql
select * from employees where hire_date between '1986-12-29' and '1986-12-31' order by hire_date;
```

####019. Find all those male employees who joined before 1990 with first_name as 'Bikash' and last_name as 'Juneja'. Sort the result in descending order of their birthdays.
```sql
select
    *
from
    employees
where
    hire_date < '1990-01-01'
    and first_name = 'Bikash'
    and last_name  = 'Juneja'
    and gender = 'M'
order by
    birth_date desc;
```

####020. Find those employees who joined on 3-Jan-1999 or 6-Jan-1999 or 10-March-1999 or 31-May-1999. Sort the result in ascending order of their hiring date.
```sql
select * from employees where hire_date in ('1999-01-03', '1999-01-06', '1999-03-10', '1999-05-31') order by hire_date;
```

####021. Find those employees who did NOT join on 3-Jan-1999 or 6-Jan-1999 or 10-March-1999 or 31-May-1999. Sort the result in ascending order of their hiring date.
```sql
select * from employees where hire_date NOT in ('1999-01-03', '1999-01-06', '1999-03-10', '1999-05-31') order by hire_date;
```

####022. Find those employees whose first_name has 5 characters or less.
```sql
select * from employees where length(first_name) <= 5;
```

####023. Find the employee(s) who are getting the maximum/highest salary.
```sql
```

####024. Find the employee(s) who are getting the second highest salary.
```sql
```

####025. Find the employee(s) who are getting the third highest salary.
```sql
```

####026. Find the employee(s) who are getting the Nth highest salary. Let N be 10.
```sql
```

####027. Find the employee(s) who got the maximum salary in the year 2002.
```sql
```

####028. List emp_no, first_name, last_name and salary of the youngest employee.
```sql
```

####029. List emp_no, first_name, last_name and salary of the youngest female employee.
```sql
```

####030. List emp_no, first_name, last_name and salary of the oldest male employee.
```sql
```

####031. Find the employee(s) who are earning salaries between 155000 and 160000.
```sql
```

####032. Find all those employee(s) whose salary is more than the salary of Mr Bikash Morton.
```sql
```

####033. Find all those employee(s) whose salary is same as Mr Bikash Morton's salary or Somnath Foote's salary. Sort the result in descending order of their salaries.
```sql
```

####034. Find the number of employees whose salary is greater than the current average salary.
```sql
```

####035. Find the average salary of all those employees who have more than 10 years of work experience.
```sql
```

####036. List all those employees whose salary is a multiple of 500. OR List all those employees whose salary ends with '500'.
```sql
```

####037. List all the employees whose annual salary is more than 1.8 million.
```sql
```

####038. List all the employees whose daily salary is more than 5151.
```sql
```

####039. List the total number of male and female employees along with their average, maximum and minimum salaries.
```sql
```

####040. What is the salary that is given to the maximum number of employees. How many such employees are there.
```sql
```