# DBMS

-- born after> 1889 0r points > 1000 AND live in Virgiina (VA)

SELECT *
FROM customers
Where birth_date > '1889-01-01'OR points> '1000' AND state ='VA';


-- ORDER:
-- 1. AND
-- 2.OR
-- 3.NOT


SELECT *
FROM customers
Where birth_date > '1989-01-01'AND points> '1000' OR state ='VA';


SELECT *
FROM customers
WHERE NOT (state = 'FL');

USE store;
-- Get top3 customers

select*
FROM customers
LIMIT 3;


 -- exercise: Get top 3 loyal customers
  
  select*
  FROM customers
  order by points DESC
  LIMIT 3;
  

 
 
-- thE LIMIT clause should always come at the end.
-- The order of the clauses matter. SELECT -> FROM -> optionally WHERE -> optionally ORDER BY -> LIMIT
-- Not following the order gives error.





-- If the argument is greater than the number of customers, then we get all the customers.
-- Pagination
-- page 1: 1-3
-- page 2: 4-6
-- page 3: 7-9
-- Get customers on Page 3


USE exercise_hr;

SELECT*
FROM employees;


SELECT*
FROM employees
WHERE first_name = 'Lex';

EXPLAIN SELECT*
FROM employess 
WHERE last_name = 'De Haan';






CREATE DATABASE IF NOT EXISTS project;

CREATE TABLE IF NOT EXISTS user (
username VARCHAR(50) PRIMARY KEY,
password VARCHAR(50),
dob DATE,
phone VARCHAR(20),
email VARCHAR(100),
first_name VARCHAR(50),
last_name VARCHAR(50),
whatsapp_no VARCHAR(20)
);
ALTER TABLE whatsapp_no;
DESCRIBE user;
/*
Numbers : INT, BIGINT
Decimal numbers (eg. 3.14) : DOUBLE
Strings:
		-- if fixed length: CHAR(2)
        -- if variable length: VARCHAR(255)
Date: DATE
Datetime: DATETIME
Boolean: TINYINT
*/
use project;
ALTER TABLE project
ADD whatsapp_no INT;
DESCRIBE user;

ALTER TABLE project
MODIFY whatsapp_no varchar(20);
DESCRIBE user;

ALTER TABLE project
DROP whatsapp_no;
DESCRIBE user;

ALTER TABLE project
RENAME COLUMN date_of_birth to dob;
DESCRIBE user;



-- Insert 10 rows into your user table.
-- Update few values in the inserted values.
-- Delete 3 rows from the inserted values.



USE exercise_hr;
	INSERT INTO user (username, password, date_of_birth, phone, email, first_name,last_name )
	VALUES ('yogesh', '16021123', '16-02-2004', 'yogesh@gmail.com', 'yogesh', 'waran');
    
    
    
INSERT INTO table2
SELECT * FROM table1
WHERE user;

    
    
 -- Write a SQL statement to create a simple table countries including columns country_id,country_name and region_id.
	
	
     
     
     CREATE TABLE countries( 
COUNTRY_ID varchar(2),
COUNTRY_NAME varchar(40),
REGION_ID decimal(10,0)
);
  
  DESC countries;
