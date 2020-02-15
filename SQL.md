https://www.sqltutorial.org/wp-content/uploads/2016/04/SQL-cheat-sheet.pdf

SQL Joins:

https://4.bp.blogspot.com/-_HsHikmChBI/VmQGJjLKgyI/AAAAAAAAEPw/JaLnV0bsbEo/s1600/sql%2Bjoins%2Bguide%2Band%2Bsyntax.jpg

## Khan Academy

### Creating a table and inserting data

```js
/** Grocery list: 
Bananas (4)
Peanut Butter (1)
Dark Chocolate Bars (2)
**/

CREATE TABLE groceries (id INTEGER PRIMARY KEY, name TEXT, quantity INTEGER );

INSERT INTO groceries VALUES (1, "Bananas", 4);
INSERT INTO groceries VALUES (2, "Peanut Butter", 1);
INSERT INTO groceries VALUES (3, "Dark chocolate bars", 2);
```

### Querying the table

```js
CREATE TABLE groceries (id INTEGER PRIMARY KEY, name TEXT, quantity INTEGER, aisle INTEGER);
INSERT INTO groceries VALUES (1, "Bananas", 4, 7);
INSERT INTO groceries VALUES(2, "Peanut Butter", 1, 2);
INSERT INTO groceries VALUES(3, "Dark Chocolate Bars", 2, 2);
INSERT INTO groceries VALUES(4, "Ice cream", 1, 12);
INSERT INTO groceries VALUES(5, "Cherries", 6, 2);
INSERT INTO groceries VALUES(6, "Chocolate syrup", 1, 4);

SELECT * FROM groceries ORDER BY aisle;                      // order ascending by aisle


id	name	              quantity	aisle
2	Peanut Butter	     1     	2
3	Dark Chocolate Bars	2	     2
5	Cherries	          6	     2
6	Chocolate syrup	1	     4
1	Bananas	          4	     7
4	Ice cream	          1	     12


SELECT * FROM groceries WHERE aisle > 5 ORDER BY aisle;      // order ascending by aisle WHERE aisle > 5

id	name	     quantity	aisle
1	Bananas	    4	7
4	Ice cream	    1	12
```

### Aggregating data

```js
SELECT SUM(quantity) FROM groceries;             // sum up all rows in quantity column

SUM(quantity)
15


SELECT MAX(quantity) FROM groceries;             // return biggest numb

SUM(quantity)
6


SELECT aisle, SUM(quantity) FROM groceries GROUP BY aisle;     // returns ALL aisles reduced + SUM of Quantity for EACH aisle with SAME aisle  NUMBER

aisle	SUM(quantity)
2	      9
4	      1
7	      4
12	      1

SELECT type, SUM(calories) AS total_calories FROM exercise_logs GROUP BY type;

// using AS we change the colum name from CALORIES to TOTAL_CALORIES

https://www.khanacademy.org/computing/computer-programming/sql/sql-basics/pp/project-design-a-store-database
```

### Complex queries with AND/OR

```js
CREATE TABLE exercise_logs
    (id INTEGER PRIMARY KEY AUTOINCREMENT,
    type TEXT,
    minutes INTEGER, 
    calories INTEGER,
    heart_rate INTEGER);


INSERT INTO exercise_logs(type, minutes, calories, heart_rate) VALUES ("biking", 30, 100, 110);
INSERT INTO exercise_logs(type, minutes, calories, heart_rate) VALUES ("biking", 10, 30, 105);
INSERT INTO exercise_logs(type, minutes, calories, heart_rate) VALUES ("dancing", 15, 200, 120);


SELECT * FROM exercise_logs WHERE calories > 50 AND minutes < 30;         /* AND */

id	type	     minutes	calories	heart_rate
3	dancing	15	       200	120


SELECT * FROM exercise_logs WHERE calories > 50 OR heart_rate > 100;      /* OR */

id	type	     minutes	calories	heart_rate
1	biking	30	       100	110
2	biking	10	        30	105
3	dancing	15	       200	120
```

### Querying IN subqueries

```js
// instead of using:

SELECT * FROM exercise_logs WHERE type = "biking" OR type = "hiking" OR type = "tree climbing" OR type = "rowing";

// we use IN:

SELECT * FROM exercise_logs WHERE type IN ("biking", "hiking", "tree climbing", "rowing");

// reverse of IN -> NOT IN

SELECT * FROM exercise_logs WHERE type NOT IN ("biking", "hiking", "tree climbing", "rowing");
```

### INNER QUERY (subquery)

```js
CREATE TABLE drs_favorites
    (id INTEGER PRIMARY KEY,
    type TEXT,
    reason TEXT);

INSERT INTO drs_favorites(type, reason) VALUES ("biking", "Improves endurance and flexibility.");
INSERT INTO drs_favorites(type, reason) VALUES ("hiking", "Increases cardiovascular health.");



SELECT type FROM drs_favorites;

SELECT * FROM exercise_logs WHERE type IN (
    SELECT type FROM drs_favorites);             // inner query, returns ALL from exercise_logs that MATCH TYPE from drs_favorites


SELECT * FROM exercise_logs WHERE type IN (
    SELECT type FROM drs_favorites WHERE reason = "Increases cardiovascular health");   // more specific return based on TYPE AND REASON
    
    
/* LIKE */

SELECT * FROM exercise_logs WHERE type IN (
    SELECT type FROM drs_favorites WHERE reason LIKE "%cardiovascular%");   // returns all with KEYWORD

```

##### EXAMPLE - 2 tables:
```js
// To finish creating the 'Pop' playlist, add another query that will select the title of all the songs from the 'Pop' artists. It should use IN on a nested subquery that's based on your previous query.


SELECT title FROM songs WHERE artist = 'Queen';

SELECT name FROM artists WHERE genre = 'Pop';

SELECT title FROM songs WHERE artist IN (SELECT name FROM artists WHERE genre = "Pop" AND name = artist);

// returns TITLE from SONGS where ARTIST in artist table has genre 'Pop' and name MATHING to TITLE from songs
```

### Restricting grouped results with HAVING

```js
SELECT type, SUM(calories) AS total_calories FROM exercise_logs
    GROUP BY type
    HAVING total_calories > 150
    ;

SELECT type, AVG(calories) AS avg_calories FROM exercise_logs
    GROUP BY type
    HAVING avg_calories > 70
    ; 
    
SELECT type FROM exercise_logs GROUP BY type HAVING COUNT(*) >= 2;      // returns TYPE whos ROW shows up in table >= 2 times
```

##### EXAMPLE
```js
// In this first step, select all the authors who have written more than 1 million words, using GROUP BY and HAVING. Your results table should include the 'author' and their total word count as a 'total_words' column.

SELECT author, SUM(words) AS total_words FROM books GROUP BY author HAVING total_words > 1000000;

author	        total_words
J.K. Rowling	1086594


SELECT author, AVG(words) AS avg_words FROM books GROUP BY author HAVING avg_words > 150000;    // AVERAGE
```

### Calculating results with CASE

```js
SELECT * FROM exercise_logs;

id	type	        minutes	calories	heart_rate
1	biking	            30	    100	        110
2	biking	            10	    30	        105
3	dancing	            15	    200	        120 
4	dancing	            15	    165	        120
5	tree climbing	    30	    70	         90
6	tree climbing	    25	    72	         80
7	rowing	            30	    70	         90
8	hiking	            60	    80	         85



SELECT COUNT(*) FROM exercise_logs WHERE heart_rate > 220 - 30;

COUNT(*)
0



/* 50-90% of max*/
SELECT COUNT(*) FROM exercise_logs WHERE
    heart_rate >= ROUND(0.50 * (220-30)) 
    AND  heart_rate <= ROUND(0.90 * (220-30));
    
COUNT(*)
4



/* CASE */
SELECT type, heart_rate,
    CASE 
        WHEN heart_rate > 220-30 THEN "above max"                      // creates new column and assigns value of TYPE and HEART_RATE
        WHEN heart_rate > ROUND(0.90 * (220-30)) THEN "above target"
        WHEN heart_rate > ROUND(0.50 * (220-30)) THEN "within target"
        ELSE "below target"
    END as "hr_zone"
FROM exercise_logs;


type	        heart_rate	    hr_zone
biking	            110	        within target
biking	            105	        within target
dancing	            120	        within target
dancing	            120	        within target
tree climbing	    90	        below target
tree climbing	    80	        below target
rowing	            90	        below target
hiking	            85	        below target



SELECT COUNT(*),                // returns total count grouped by the number of HR_ZONE
    CASE 
        WHEN heart_rate > 220-30 THEN "above max"
        WHEN heart_rate > ROUND(0.90 * (220-30)) THEN "above target"
        WHEN heart_rate > ROUND(0.50 * (220-30)) THEN "within target"
        ELSE "below target"
    END as "hr_zone"
FROM exercise_logs
GROUP BY hr_zone;


COUNT(*)	hr_zone
4	        below target
4	        within target   
```

## Relational Queries in SQL

https://www.khanacademy.org/computing/computer-programming/sql/relational-queries-in-sql/pt/joining-related-tables

```js
// Old Table with all data:

student_name	    book_title	                    book_author
Peter Rabbit	    The Tale of Mrs. Tiggy-Winkle	Beatrix Potter
Peter Rabbit	    Jabberwocky	                    Lewis Carroll
Alice Wonderland	The Hunting of the Snark	    Lewis Carroll
Alice Wonderland	Jabberwocky	                    Lewis Carroll
```

```js
// New Tables with seperated data:

student_id	student_name	    
1	        Peter Rabbit	    
2	        Alice Wonderland	
1	        Peter Rabbit	    
2	        Alice Wonderland	


id	book_title	                    book_author
1	The Tale of Mrs. Tiggy-Winkle	Beatrix Potter
2	Jabberwocky	                    Lewis Carroll
3	The Hunting of the Snark	    Lewis Carroll
```

```js
// JOIN TABLE we use to connect:

student_id	book_id
1	            1
1	            2
2	            3
2	            2
```

There are several types of `database relationship`:

- One to One 
- One-to-Many (or Many-to-One) 
- Many to Many -> linked by an intermediary table.

When selecting data from multiple tables with relationships, we will be using the JOIN query. 

- Cross Joins
- Natural Joins
- Inner Joins
- Left (Outer) Joins
- Right (Outer) Joins

https://database.guide/the-3-types-of-relationships-in-database-design/

##### TABLES

```js
CREATE TABLE students (id INTEGER PRIMARY KEY,
    first_name TEXT,
    last_name TEXT,
    email TEXT,
    phone TEXT,
    birthdate TEXT);
    
CREATE TABLE student_grades (id INTEGER PRIMARY KEY,
    student_id INTEGER,
    test TEXT,
    grade INTEGER);
```

#### Cross Join

```js
// 2 tables, student_grades, students

SELECT * FROM student_grades, students;
```

#### Inner Join

```js
/* implicit inner join */                       // joinst 2 tables in to 1

SELECT * FROM student_grades, students
    WHERE student_grades.student_id = students.id;
    
    
id	student_id	test	    grade	id	first_name	last_name	email	                phone	    birthdate
1	1	        Nutrition	95	    1	Peter	    Rabbit	    peter@rabbit.com	    555-6666	2002-06-24
2	2	        Nutrition	92	    2	Alice	    Wonderland	alice@wonderland.com	555-4444	2002-07-04
3	1	        Chemistry	85	    1	Peter	    Rabbit	    peter@rabbit.com	    555-6666	2002-06-24
4	2	        Chemistry	95	    2	Alice	    Wonderland	alice@wonderland.com	555-4444	2002-07-04    

// SAME RESULT different way:

/* explicit inner join - JOIN */

SELECT * FROM students
    JOIN student_grades
    ON students.id = student_grades.student_id;
```

```js
/* explicit inner join - JOIN */

SELECT students.first_name, students.last_name, students.email, student_grades.test, student_grades.grade FROM students
    JOIN student_grades                                              // joining with other table = JOINED TABLE
    ON students.id = student_grades.student_id                       // where to join with conditional
    WHERE grade > 90;                                                // additional where conditional to return selected value 


first_name	last_name	email	                test	    grade
Peter	    Rabbit	    peter@rabbit.com	    Nutrition	95
Alice	    Wonderland	alice@wonderland.com	Nutrition	92
Alice	    Wonderland	alice@wonderland.com	Chemistry	95
```

### Stack O example


Suppose you have two tables, with a single column each, and data as follows:
```js
A    B
-    -
1    3
2    4
3    5
4    6
```

Note that (1,2) are unique to A, (3,4) are common, and (5,6) are unique to B.

##### Inner join

An inner join using either of the equivalent queries gives the intersection of the two tables, i.e. the two rows they have in common.

```js
SELECT * FROM a 
    INNER JOIN b 
    ON a.a = b.b;

a | b
--+--
3 | 3
4 | 4
```

##### Left outer join

A left outer join will give all rows in A, plus any common rows in B.

```js
SELECT * FROM a
    LEFT OUTER JOIN b 
    ON a.a = b.b;

a |  b
--+-----
1 | null
2 | null
3 |    3
4 |    4
```

##### Right outer join

A right outer join will give all rows in B, plus any common rows in A.

```js
SELECT * FROM a 
    RIGHT OUTER JOIN b 
    ON a.a = b.b;

a    |  b
-----+----
3    |  3
4    |  4
null |  5
null |  6
```

##### Full outer join

A full outer join will give you the union of A and B, i.e. all the rows in A and all the rows in B. If something in A doesn't have a corresponding datum in B, then the B portion is null, and vice versa.

```js
SELECT * FROM a 
    FULL OUTER JOIN b 
    ON a.a = b.b;

 a   |  b
-----+-----
   1 | null
   2 | null
   3 |    3
   4 |    4
null |    6
null |    5
```



## SQL Tutorial

### Querying data from a table

Query data in columns c1, c2 from a table

```
SELECT c1, c2 FROM t;
```

##### Query all rows and columns from a table

```
SELECT * FROM t;
```

##### Query data and filter rows with a condition

```
SELECT c1, c2 FROM t
WHERE condition;
```

##### Query distinct rows from a table

```
SELECT DISTINCT c1 FROM t
WHERE condition;
```

##### Sort the result set in ascending or descending order

```
SELECT c1, c2 FROM t
ORDER BY c1 ASC [DESC];
```

##### Skip offset of rows and return the next n rows

```
SELECT c1, c2 FROM t
ORDER BY c1 
LIMIT n OFFSET offset;
```

##### Group rows using an aggregate function

```
SELECT c1, aggregate(c2)
FROM t
GROUP BY c1;
```

##### Filter groups using HAVING clause

```
SELECT c1, aggregate(c2)
FROM t
GROUP BY c1
HAVING condition;
```

### Querying from multiple tables

##### Inner join t1 and t2

```
SELECT c1, c2 
FROM t1
INNER JOIN t2 ON condition;
```

##### Left join t1 and t1

```
SELECT c1, c2 
FROM t1
LEFT JOIN t2 ON condition;
```

##### Right join t1 and t2

```
SELECT c1, c2 
FROM t1
RIGHT JOIN t2 ON condition;
```

##### Perform full outer join

```
SELECT c1, c2 
FROM t1
FULL OUTER JOIN t2 ON condition;
```

##### Produce a Cartesian product of rows in tables

```
SELECT c1, c2 
FROM t1
CROSS JOIN t2;
```

##### Another way to perform cross join

```
SELECT c1, c2 
FROM t1, t2;
```

##### Join t1 to itself using INNER JOIN clause

```
SELECT c1, c2
FROM t1 A
INNER JOIN t2 B ON condition;
```

### Using SQL Operators

##### Combine rows from two queries

```
SELECT c1, c2 FROM t1
UNION [ALL]
SELECT c1, c2 FROM t2;
```

##### Return the intersection of two queries

```
SELECT c1, c2 FROM t1
INTERSECT
SELECT c1, c2 FROM t2;
```

##### Subtract a result set from another result set

```
SELECT c1, c2 FROM t1
MINUS
SELECT c1, c2 FROM t2;
```

##### Query rows using pattern matching %, _

```
SELECT c1, c2 FROM t1
WHERE c1 [NOT] LIKE pattern;
```

##### Query rows in a list

```
SELECT c1, c2 FROM t
WHERE c1 [NOT] IN value_list;
```

##### Query rows between two values

```
SELECT c1, c2 FROM t
WHERE  c1 BETWEEN low AND high;
```

##### Check if values in a table is NULL or not

```
SELECT c1, c2 FROM t
WHERE  c1 IS [NOT] NULL;
```

### Managing tables

##### Create a new table with three columns

```
CREATE TABLE t (
     id INT PRIMARY KEY,
     name VARCHAR NOT NULL,
     price INT DEFAULT 0
);
```

##### Delete the table from the database

```
DROP TABLE t ;
```

##### Add a new column to the table

```
ALTER TABLE t ADD column;
```

##### Drop column c from the table

```
ALTER TABLE t DROP COLUMN c ;
```

##### Add a constraint

```
ALTER TABLE t ADD constraint;
```

##### Drop a constraint

```
ALTER TABLE t DROP constraint;
```

##### Rename a table from t1 to t2

```
ALTER TABLE t1 RENAME TO t2;
```

##### Rename column c1 to c2

```
ALTER TABLE t1 RENAME c1 TO c2 ;
```

##### Remove all data in a table

```
TRUNCATE TABLE t;
```

### Using SQL constraints

##### Set c1 and c2 as a primary key

```
CREATE TABLE t(
    c1 INT, c2 INT, c3 VARCHAR,
    PRIMARY KEY (c1,c2)
);
```

##### Set c2 column as a foreign key

```
CREATE TABLE t1(
    c1 INT PRIMARY KEY,  
    c2 INT,
    FOREIGN KEY (c2) REFERENCES t2(c2)
);
```

##### Make the values in c1 and c2 unique

```
CREATE TABLE t(
    c1 INT, c1 INT,
    UNIQUE(c2,c3)
);
```

##### Ensure c1 > 0 and values in c1 >= c2

```
CREATE TABLE t(
  c1 INT, c2 INT,
  CHECK(c1> 0 AND c1 >= c2)
);
```

##### Set values in c2 column not NULL

```
CREATE TABLE t(
     c1 INT PRIMARY KEY,
     c2 VARCHAR NOT NULL
);
```

### Modifying Data

##### Insert one row into a table

```
INSERT INTO t(column_list)
VALUES(value_list);
```

##### Insert multiple rows into a table

```
INSERT INTO t(column_list)
VALUES (value_list), 
       (value_list), …;
```

##### Insert rows from t2 into t1

```
INSERT INTO t1(column_list)
SELECT column_list
FROM t2;
```

##### Update new value in the column c1 for all rows

```
UPDATE t
SET c1 = new_value;
```

##### Update values in the column c1, c2 that match the condition

```
UPDATE t
SET c1 = new_value, 
        c2 = new_value
WHERE condition;
```

##### Delete all data in a table

```
DELETE FROM t;
```

##### Delete subset of rows in a table

```
DELETE FROM t
WHERE condition;
```

### Managing Views

##### Create a new view that consists  of c1 and c2

```
CREATE VIEW v(c1,c2) 
AS
SELECT c1, c2
FROM t;
```

##### Create a new view with check option

```
CREATE VIEW v(c1,c2) 
AS
SELECT c1, c2
FROM t;
WITH [CASCADED | LOCAL] CHECK OPTION;
```

##### Create a recursive view

```
CREATE RECURSIVE VIEW v 
AS
select-statement -- anchor part
UNION [ALL]
select-statement; -- recursive part
```

##### Create a temporary view

```
CREATE TEMPORARY VIEW v 
AS
SELECT c1, c2
FROM t;
```

##### Delete a view

```
DROP VIEW view_name;
```

### Managing indexes

##### Create an index on c1 and c2 of the t table

```
CREATE INDEX idx_name 
ON t(c1,c2);
```

##### Create a unique index on c3, c4 of the t table

```
CREATE UNIQUE INDEX idx_name
ON t(c3,c4)
```

##### Drop an index

```
DROP INDEX idx_name;
```

### Managing triggers

##### Create or modify a trigger

```
CREATE OR MODIFY TRIGGER trigger_name
WHEN EVENT
ON table_name TRIGGER_TYPE
EXECUTE stored_procedure;
```

WHEN

  BEFORE – invoke before the event occurs
  AFTER – invoke after the event occurs

EVENT

  INSERT – invoke for INSERT
  UPDATE – invoke for UPDATE
  DELETE – invoke for DELETE

TRIGGER_TYPE

  FOR EACH ROW
  FOR EACH STATEMENT

##### Delete a specific trigger

```
DROP TRIGGER trigger_name;
```
