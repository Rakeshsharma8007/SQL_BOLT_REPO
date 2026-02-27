<center><h2>EXERCISE 12</h2></center>
<h4>Queries:</h4>

### 1.Find the number of movies each director has directed.
~~~sql
SELECT director, COUNT(id) as movies_directed
FROM movies
GROUP BY director;
~~~
### 2.Find the total domestic and international sales that can be attributed to each director.
~~~sql
SELECT director, 
       SUM(domestic_sales) AS total_domestic, 
       SUM(international_sales) AS total_international
FROM movies
JOIN boxoffice
  ON movies.id = boxoffice.movie_id
GROUP BY director;
~~~
