<center><h2>EXERCISE 8</h2></center>
<h4>Queries:</h4>

### 1.Find the name and role of all employees who have not been assigned to a building.
~~~sql
SELECT name, role 
FROM employees
WHERE building IS NULL;
~~~
### 2.Find the names of the buildings that hold no employees.
~~~sql
SELECT building_name
FROM buildings
  LEFT JOIN employees
  ON buildings.building_name = employees.building
WHERE name IS NULL;
~~~
