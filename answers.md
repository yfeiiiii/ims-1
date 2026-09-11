Create_table.sql

Q1: What do you think that this file does? What columns are created? What data types are stored in our columns? And which size is the data allowed to be? Which column hold the primary key (and why?) What do you think AUTO_INCREMENT does?

A1: 
This file creates a table in a database. 
The columns are ID, name, domain and propulsion. 
The size is VARCHAR(255), which is variable character with maximum length of 255. 
The primary key is ID, because it's unique.
AUTO_INCREMENT is for maintaining the uniqueness of IDs.

Get_data.php

Q1 Observe on line 1 and 28 that we need to open and close a .php file. Write down the syntax to do so.

A1 <?php to open and ?> to close it.

Q2 Observe on line 2-5 that we are creating variables. Write down the syntax to create a variable in php.

A2 $variable_name = "integer/string"

Q3 For each of the variables on line 2-5, describe what they are. What values should they hold in your case? 
Line 8: what variable is created here, and why? What do you think is the purpose of line 10-12, why do we need this?

A3 The servername represents the server; username and password mean the information that the user needs to connect to the server; dbname represents the database.
For line8, $link is created to connect to the database. If the connection fails, it calls die, so the execution will be stopped. 

Q4 Line 14: What does echo do? What would you call this statement in other programming languages you know?

A4 Echo prints the information. 'print'

Q5 Line 14: you can see HTML code here. What do you think this echo statement returns?

A5 It returns the html-formated code to the browser and it returns a table with ID, name, domain and propulsion.

Q6 Line 17: here we are calling our $link variable. Why do you think that is? Here we introduce a new operator: “->”. Why do you think this operator is useful? Here we introduce a new method, query. What do you think this method does, and which parameter do we use?

A6 It tells php which database it should point to. “->” makes sure the specific query is execuated based on the connection of server and database.


Q7 On line 19: we observe that num_rows is not coloured yellow like our methods. At the same time, it is not a variable either, since it does not start with $. We call this a property access. What are we accessing, and from where?

A7 num_rows is a built-in data that count the number of rows of the query. 

Q8 Line 19 - 25: a conditional loop is introduced. Can you guess what the output is of this code? Under which conditions?

Q8: fetch_assoc() gets each column's value if there's some information from the database. If the table is empty, it'll print "0 results". Or else it'll print the table row by row.

Index.php

Q1: Can you guess what the purpose is of this file? Hint: Think about your IMS. If the user is on the index page, where would they be?

A1: The file is the default file a server loads when no specific page is requested.

Insert_data.html
Q1: What do you think a form is in HTML?
A1: It lets the user input data.

Insertdata.php
Q1: Line 16-21. What do you think the $_POST superglobal does?
A1: $_POST holds the data from user input data.

Q2: Line 23: here we prepare a SQL query. Why do you think the values are left blank for now? (?,?,?)
A2: '?' are placeholders, it will be replaced by input data.

Q3: Line 27: Even though we have $_POST[‘id’] data, we do not enter this into our database! Why is that? Think about our first file, create_table.sql
A3: Because MySQL generates this value automatically every time a new row is inserted because of the AUTO_INCREMENT defined previously.


Q4: Line 36: Close db connection. This is the first time we see this. Why does it occur here?
A5: Once all quries are done, the connection doesn't need to be opened. Frees up memory/resources.





