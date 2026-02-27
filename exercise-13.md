<center><h2>EXERCISE 13</h2></center>
<h4>Queries:</h4>

### 1.Add the studio's new production, Toy Story 4 to the list of movies (you can use any director).
~~~sql
SELECT director, COUNT(*) as movie_count
FROM movies
GROUP BY director;
~~~
### 2.Toy Story 4 has been released to critical acclaim! It had a rating of 8.7, and made 340 million domestically and 270 million internationally. Add the record to the BoxOffice table.
~~~sql
SELECT director, 
       SUM(domestic_sales) AS total_domestic_sales, 
       SUM(international_sales) AS total_international_sales
FROM movies
  JOIN boxoffice
    ON movies.id = boxoffice.movie_id
GROUP BY director;
~~~
