[Main Page](https://github.com/davidj778/davidj778)

# Apply filters to SQL queries


## Project description

[Describe what you accomplish through SQL.]


## Retrieve after hours failed login attempts


```
SELECT *
FROM log_in_attempts
WHERE login_time > ‘18:00’ AND success = FALSE;
```

In order to view all columns, we used the SELECT command, followed by the asterisk sign, which means select all columns. Next, we used the WHERE command to define certain rules that we want to apply to our table were login times would be greater than 18:00(login_time > ‘18:00’) and the amount of false login attempts(success = FALSE). The AND logical operator combines both parameters to the statement.

## Retrieve login attempts on specific dates

```
SELECT *
FROM log_in_attempts
WHERE login_date = ‘2022-05-08’ OR login_date = ‘2022-05-09’;
```

For the retrieval of login attempts on specific dates, we again used the SELECT and FROM commands to create our table based on which table we want and which columns. To retrieve the login dates we want, we used the WHERE command followed by the name of the column(login_date) to equal either ‘2022-05-08’ or ‘2022-05-09’. The OR operator gives the option to display either dates.

## Retrieve login attempts outside of Mexico

```
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE ‘MEX%’;
```

As before, we used the SELECT and FROM commands to retrieve the usual data. All of the columns from the table log_in_attempts. Since we don’t want a certain country to be listed in this query, we used the NOT operator for the country column followed by the LIKE keyword in combination with the % wildcard to not query any result that has “MEX” with anything else.

## Retrieve employees in Marketing

```
SELECT *
FROM employees
WHERE department = ‘Marketing’ AND office LIKE ‘East%’;
```

For this query we used the WHERE command to generate 2 columns. The department columns to display anything that has the word “Marketing” and the columns office to display “East”, followed by anything else. As before the LIKE keyword used with the % wildcard allows for this search type.

## Retrieve employees in Finance or Sales

```
SELECT *
FROM employees
WHERE department = ‘Sales’ OR department = ‘Finance’;
```

In order to retrieve finance and sales employees, the WHERE command is used to filter “Sales” and “Finance” for the column “department".

## Retrieve all employees not in IT

```
SELECT *
FROM employees
WHERE NOT department = ‘Information Technology’;
```

Finally, we used the SELECT command followed by the asterisk to provide all columns. Then we choose the employees table using the FROM command. In this query, we did not want any of our results to show the IT department. We used the WHERE command combined with the NOT operator to not display the Information Technology department.

## Summary







