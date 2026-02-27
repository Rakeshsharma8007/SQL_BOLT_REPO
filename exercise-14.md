<center><h2>EXERCISE 14</h2></center>
<h4>Queries:</h4>

### 1.The director for A Bug's Life is incorrect, it was actually directed by John Lasseter.
### 2.
~~~sql
SELECT director, COUNT(*) as movie_count
FROM movies
GROUP BY director;
~~~
### 2.The year that Toy Story 2 was released is incorrect, it was actually released in 1999.
~~~sql
UPDATE movies
SET year = 1999
WHERE title = "Toy Story 2";
~~~
### 3.Both the title and director for Toy Story 8 is incorrect! The title should be "Toy Story 3" and it was directed by Lee Unkrich.
~~~sql
UPDATE movies
SET title = "Toy Story 3", 
    director = "Lee Unkrich"
WHERE title = "Toy Story 8";
~~~
