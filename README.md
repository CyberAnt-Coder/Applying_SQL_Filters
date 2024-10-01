# Applying_SQL_Filters

## Description
In this lab, I used SQL to investigate a potential security incident in a fictional company. The potential securtiy incident occurred after business hours so I used SQL queries to identify all failed login attempts that occurred after 18:00.

# Walkthrough:

## Retrieve after hours failed login attempts
Since the potential security incident occurred after business hours, all failed login attempts made after 18:00 should be investigated. Therefore my query would be:<br>
![failedloginattempts](https://i.imgur.com/9prKUDL.png)
<br>
First I chose to `SELECT` all information with the `*` from the `log_in_attempts table`. I then used the `WHERE` and `AND` operator to filter the output to only results with a login attempt made after business hours and a failed login attempt.

## Retrieve login attempts on specific dates
Since the suspicious event occurred on 2022/05/09, any login attempt on that day or the day before should be investigated. My query is as follows:<br>
![specificdates](https://i.imgur.com/y43gTP4.png)
<br>
The query would return all data from the `log_in_attempts table`, but this time I used the operators `WHERE` and `OR` to specify the 2 specific dates we wished to investigate‘2022-05-09’ and ‘2022-05-08’. 

## Retrieve login attempts made outside of Mexico
After reviewing the organization's data, there appears to be an issue with the login attempts made outside of Mexico. To find the attempts made outside of Mexico my query would be as follows:<br>
![notmex](https://imgur.com/QHMLmyA.png)
<br>
The query would return all data from the `log_in_attempts table`, but this time I used the operators `WHERE` and `NOT` to filter for countries other than Mexico. After I used `LIKE` and `MEX%` as the pattern to match to as the dataset represents Mexico as `MEX` and `MEXICO`. The `%` sign represents any number of unspecified characters when used with the `LIKE` operator.

## Retrieve employees in Marketing
Next the team wanted to update the computers for employees in the Marketing department. To do this, I used the following query to find which employee machines to update:<br>
![marketing](https://imgur.com/8dTsNBw.png)
<br>
The query would return all data from the `employees` table, I then filtered it using `WHERE` and `AND` operators to specify Marketing workers from the East office. I used `LIKE` with `EAST%` to pattern match it as the data in the `office` column ends with different numbers.

## Retrieve employees in Finance or Sales
The machines in Finance and Sales must also be updated, so to filter for these two departments I used the following query:<br>
![financeorsales](https://imgur.com/s76a2AA.png)<br>
The query would return all data from the `employees` table, I then filtered it using `WHERE` and `OR` operators to get the workers in either Sales or Finance. I used the `OR` operator instead of `AND` as I wanted employees in either department, not employees in both departments.
## Retrieve all employees not in IT
The team then requested one more security update on employees who are not in the IT department. To make the update, I first had to find all the employees not in the IT department using the following query:<br>
![notit](https://imgur.com/nZuabVu.png)
<br>
The query would return all data from the `employees` table, I then filtered it using the `WHERE` and `NOT` operators. I used the `NOT` operator to specify all other departments except IT. 
## Summary
This was a showcase where I applied my knowledge of SQL queries in order to get specific information. I used the two tables `employees` and `log_in_attempts`. I also used multiple operators such as `AND`, `OR`, and `NOT` to complete each task. I also used the `LIKE` operator along with the `%` to filter for patterns in certain columns.
