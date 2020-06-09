SQL (Structured Query Language) is a language used to interact with relational databases. 

DBs are important for web apps in that they help store, use, and manipulate data. 
Relational DBs (like tables) are particularly useful. 

Various data types
INTEGER, DECIMAL, SERIAL, VARCHAR, TIMESTAMP, BOOLEAN, ENUM

Columns with constraints:

NOT NULL : field must have a value; if field does not have a value, entry will be rejected
UNIQUE : no two fields in this column can have the same value
PRIMARY KEY : the main way to index a table
DEFAULT : set a default value for a column if no other value is given
CHECK : bound values; e.g. values greater than 50

To create a table: 

    CREATE TABLE flights (
      id SERIAL PRIMARY KEY,
      origin VARCHAR NOT NULL,
      destination VARCHAR NOT NULL,
      duration INTEGER NOT NULL
     );
     
 
Insert data into that table: 
 
      INSERT INTO flights
      (origin, destination, duration)
      VALUES ('New York', 'London', 415);
      
      
Reading data from that table:

      SELECT * FROM flights;
      SELECT origin, destination FROM flights;
      SELECT * FROM flights WHERE id = 3;
      SELECT * FROM flights WHERE origin = 'New York';
      SELECT * FROM flights WHERE duration > 500;
      SELECT * FROM flights WHERE destination = 'Paris' AND duration > 500;
      SELECT * FROM flights WHERE destination = 'Paris' OR duration > 500;
      SELECT AVG(duration) FROM flights WHERE origin = 'New York';
      SELECT * FROM flights WHERE origin LIKE '%a%';
      SELECT * FROM flights LIMIT 2;
      SELECT * FROM flights ORDER BY duration ASC;
      SELECT * FROM flights ORDER BY duration ASC LIMIT 3;
      SELECT origin, COUNT(*) FROM flights GROUP BY origin;
      SELECT origin, COUNT(*) FROM flights GROUP BY origin HAVING COUNT(*) > 1;
   
 - The query after SELECT indicates what columns are being selected.
 - The query after WHERE indicates constraints on what rows are being selected.
 - * indicates ‘all’. 

Updating data in that table:
 
      UPDATE flights
      SET duration = 430
      WHERE origin = 'New York'
      AND destination = 'London';
  
Deleting data in that table:
 
      DELETE FROM flights
      WHERE destination = 'Tokyo'
      
    
Relational DBs allow us to relate various tables inside them to each other. We could
reference the id column in one table in another column of some other table. 

Potential problems with SQL and DBs
1. SQL injection attacks. Example: Putting cleverly placed single-quotes in order to edit 
the SQL query. 
2. Race conditions - two or more users trying to modify or gain access to a certain Db at the same time. 

SQLAlchemy is a Python library that allows Python code to run SQL commands. 




      
      
      
  
