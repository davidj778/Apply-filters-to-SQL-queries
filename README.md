[Main Page](https://github.com/davidj778/davidj778)

# Apply filters to SQL queries

## Scenario

Review the scenario below. Then complete the step-by-step instructions.

You are a security professional at a large organization. Part of your job is to investigate security issues to help keep the system secure. You recently discovered some potential security issues that involve login attempts and employee machines.
Your task is to examine the organization’s data in their employees and log_in_attempts tables. You’ll need to use SQL filters to retrieve records from different datasets and investigate the potential security issues.

## Project description

There has been recent login attempts and other issues with employee machines that have become a potential security issue. The goal is to examine the logins and machines using the sql query to determine if there is a problem that needs to be addressed.


## Retrieve after hours failed login attempts


```
SELECT *
FROM log_in_attempts
WHERE login_time > ‘18:00’ AND success = FALSE;
```

In order to view all columns, we used the SELECT keyword, followed by the asterisk sign, which means select all columns. Next, we used the WHERE keyword to define certain rules that we want to apply to our table were login times would be greater than 18:00(login_time > ‘18:00’) and the amount of false login attempts(success = FALSE). The AND logical operator combines both parameters to the statement.

## Retrieve login attempts on specific dates

```
SELECT *
FROM log_in_attempts
WHERE login_date = ‘2022-05-08’ OR login_date = ‘2022-05-09’;
```

For the retrieval of login attempts on specific dates, we again used the SELECT and FROM keywords to create our table based on which table we want and which columns. To retrieve the login dates we want, we used the WHERE keyword followed by the name of the column(login_date) to equal either ‘2022-05-08’ or ‘2022-05-09’. The OR operator gives the option to display either dates.

## Retrieve login attempts outside of Mexico

```
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE ‘MEX%’;
```

As before, we used the SELECT and FROM keywords to retrieve the usual data. All of the columns from the table log_in_attempts. Since we don’t want a certain country to be listed in this query, we used the NOT operator for the country column followed by the LIKE keyword in combination with the % wildcard to not query any result that has “MEX” with anything else.

## Retrieve employees in Marketing

```
SELECT *
FROM employees
WHERE department = ‘Marketing’ AND office LIKE ‘East%’;
```

For this query we used the WHERE keyword to generate 2 columns. The department columns to display anything that has the word “Marketing” and the columns office to display “East”, followed by anything else. As before the LIKE keyword used with the % wildcard allows for this search type.

## Retrieve employees in Finance or Sales

```
SELECT *
FROM employees
WHERE department = ‘Sales’ OR department = ‘Finance’;
```

In order to retrieve finance and sales employees, the WHERE keyword is used to filter “Sales” and “Finance” for the column “department".

## Retrieve all employees not in IT

```
SELECT *
FROM employees
WHERE NOT department = ‘Information Technology’;
```

Finally, we used the SELECT keyword followed by the asterisk to provide all columns. Then we choose the employees table using the FROM keyword. In this query, we did not want any of our results to show the IT department. We used the WHERE keyword combined with the NOT operator to not display the Information Technology department.

## Summary

For this project, I used the sql query to access 2 databases(log_in_attempts, employees). I also used different keywords such as AND, OR, and NOT. These keywords helped filter specific data that needed to be analyzed. The LIKE operator with the % wildcard can in handy when I needed to view certain patterns.





