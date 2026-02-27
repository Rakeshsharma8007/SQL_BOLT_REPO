<center><h2>EXERCISE 4</h2></center>
<h4>Queries:</h4>

### 1.List all directors of Pixar movies (alphabetically), without duplicates.
~~~sql
SELECT DISTINCT director FROM movies
ORDER BY director ASC;
~~~

### 2.List the last four Pixar movies released (ordered from most recent to least).
~~~sql
SELECT * FROM movies
ORDER BY year DESC
LIMIT 4;
~~~

### 3. List the first five Pixar movies sorted alphabetically.
~~~sql
SELECT * FROM movies
ORDER BY title ASC
LIMIT 5;
~~~

### 4.List the next five Pixar movies sorted alphabetically.
~~~sql
SELECT * FROM movies
ORDER BY title ASC
LIMIT 5 OFFSET 5;
~~~
