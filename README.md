# db_mySQL

| Operator | Description |
| --- | --- |
| ## | comment |

SELECT movies.movie_title, movies.year, genres.genre_title FROM movies, genres
WHERE movies.genre_id = genres.genre_id;

## select all from movies
SELECT * FROM movies ORDER BY year DESC; ## 'ASC' arrange data in ascending order for descending 'DESC';

SELECT * FROM movies ORDER BY movie_title DESC;

SELECT *  FROM movies WHERE year > 2001 ORDER BY year DESC;

SELECT * FROM movies WHERE movie_title LIKE "Co%";  ## LIKE is use for search operator


INSERT INTO `bookList`(`bookName`,`bookAuthor`) VALUES ("Nepali","anishu"),("English","anishu")
