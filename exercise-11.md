<center><h2>EXERCISE 11</h2></center>
<h4>Queries:</h4>

### 1.Find the number of Artists in the studio (without a HAVING clause).
~~~sql
SELECT COUNT(*) 
FROM employees 
WHERE role = 'Artist';
~~~
### 2.Find the number of Employees of each role in the studio.
~~~sql
SELECT role, COUNT(*) 
FROM employees 
GROUP BY role;
~~~
### 3.Find the total number of years employed by all Engineers.
~~~sql
SELECT SUM(years_employed) 
FROM employees 
WHERE role = 'Engineer';
~~~
