# sqlit_crud-using-php
A simple system (web based) using PHP programming language.
Brief Introduction:

SQLite is a relational database management system which is contained in a C programming library.
SQLite is not a client–server database engine. It is embedded into the end program. SQLite engine is not a standalone process like other databases, you can link it statically or dynamically as per your requirement with your application. The SQLite accesses its storage files directly like “my_sqlite_db_file.db” and SQLite database format or extension is “.db”. A large number of programming language is supports like C, C++, JAVA, PHP, C#, Python, GO etc.
SQLite Commands:

DDL – Data Definition Language:

CREATE Creates new table or Database
ALTER Modifies existing table.
DROP Deletes existing table or database.

DML – Data Manipulation Language:

INSERT Creates a record
UPDATE Modifies records
DELETE Deletes records

DQL – Data Query Language:

SELECT Retrieves records from tables

NOTE: All the rows of SQLite database tables has UNIQUE ID as like primary ID that name is rowid. So, you can make unique id or primary id with auto increment as like you want otherwise you can use by default rowid.
Let’s Get Started

I am going to show simple system (web based) using PHP programming language.

I am giving the project folder name “sqlit_crud” .

First Make sure your php sqlite3 extension is enable
sqlite3 enable

And now making the Database Connection file “db_connection.php”
	<?php
	// Database name
	$database_name = "my_sqlite.db";
	// Database Connection
	$db = new SQLite3($database_name);
	?>

Database connection of SQLite is a simple object of SQLite3 Class. Interesting thing you no need to create the database file it will make automatically when you make an object of SQLite3 Class. So, now we made the Database Connection where $db is the handler of Object of SQLite Class.

Okay, now we need to make a table into the Database. I am making a table “students” with two fields name as string and email as string and by default rowid will be the Primary ID.

NOTE: No need to define the rowid into Query of Creating table.

Now we need a form to insert data into table so, I am making a page “insert.php” and form in this page with post method and self action
I am checking the form is submitted or not if submitted then inserting the data into students table and setting the success or error message according to query status.
Okay, now I am going to make the list page “list.php” where all the records will show. 
Now I am going to show how to UPDATE the row data in “update.php”.
Now going to show how to delete record from table according to rowid in “delete.php”.
