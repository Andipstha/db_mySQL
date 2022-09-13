# db_mySQL

---
'##' | comment
---

SELECT movies.movie_title, movies.year, genres.genre_title FROM movies, genres
WHERE movies.genre_id = genres.genre_id;

## select all from movies
SELECT * FROM movies ORDER BY year DESC; ## 'ASC' arrange data in ascending order for descending 'DESC';

SELECT * FROM movies ORDER BY movie_title DESC;
