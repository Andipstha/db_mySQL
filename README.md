# db_mySQL

| Operator | Description |
| --- | --- |
| ## | comment |
| -- | comment |

SELECT movies.movie_title, movies.year, genres.genre_title FROM movies, genres
WHERE movies.genre_id = genres.genre_id;

## select all from movies
SELECT * FROM movies ORDER BY year DESC; ## 'ASC' arrange data in ascending order for descending 'DESC';

SELECT * FROM movies ORDER BY movie_title DESC;

SELECT *  FROM movies WHERE year > 2001 ORDER BY year DESC;

SELECT * FROM movies WHERE movie_title LIKE "Co%";  ## LIKE is use for search operator


INSERT INTO `bookList`(`bookName`,`bookAuthor`) VALUES ("Nepali","anishu"),("English","anishu")

## MySql commandeLines



| Operator | Description |
| --- | --- |
| mysql -u root -p; | show user detail |
| use <databaseName> |Select Databases |
| desc user; | show user detail |


## MySql Quarry

CREATE DATABASE name_db;

USE name_db;

CREATE TABLE Customers (
    id int auto_increment not null,
    name varchar(255),
    address varchar(255),
    primary key (id)
);


CREATE TABLE orders (
    id int auto_increment not null,
    customer_id varchar(45),
    product_id DECIMAL(5, 2),
    foreign key(customer_id) references customers(id),
    foreign key(product_id) references product(id),
);


CREATE DATABASE momo_db;

USE momo_db;

-- This is for creating customer table
CREATE TABLE customers (
    id int auto_increment not null,
    name varchar(255),
    address varchar(255),
    primary key (id)
);

CREATE TABLE product (
    productid int auto_increment not null,
    productname varchar(45),
    price DECIMAL(5, 2),
    primary key (productid)
);

INSERT INTO customers(name,address) VALUES ("sandip","kathmandu"),("ramesh","kathmandu"),("limbu","lalitpur");

CREATE TABLE orders (
    id int auto_increment not null,
    customer_id int not null,
    product_id int not null,
    foreign key(customer_id) references customers (id),
    foreign key(product_id) references product (productid),
	primary key (id)
);


INSERT INTO orders(`customer_id`,`product_id`) 
VALUES (1,1);+88889898 98

SELECT * FROM orders;

INSERT INTO product(productname,price) VALUES ("momo","100"),("chowmin","90"),("cmomo","120");

SELECT customers.name, orders.* FROM customer INNER JOIN orders ON customers.id = orders.customer_id;


