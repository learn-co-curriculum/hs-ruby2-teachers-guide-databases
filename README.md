###SWABTS
***Add a database to a Sinatra application in order to persist data***

  + DATABASES - Explain why databases are important 
  + DATABASES - Describe the structure of a database
  + SQL - Create and modify tables and access info from tables via SQL queries
  + SINATRA - Connect a Sinatra app to a DB
  + RAKE - Complete tasks using Rake (list tasks via Rake -T)
  + ACTIVE RECORD/RAKE - Understand why we use migrations
  + FORMS -  Build up and down migrations with proper syntax
  + MODEL - Understand that ActiveRecord works with models to execute SQL commands.
  + ACTIVE RECORD - Use Active Record to access data from a database



### Motivation / Why Should You Care?
The way that we use the internet would be vastly different if we couldn’t save our data. You wouldn’t be able to have sites like facebook, tumblr, yelp or pretty much anything. Databases make all of these applications possible. They are the backbone of the web. We’re going to learn how to persist (save) data so that it is accessible from different places at different times.

### Lesson Plan
**BEFORE CLASS: DOWNLOAD MYSQL** You can find the guide for downloading and using MYSQL [here](https://github.com/flatiron-school-curriculum/hs-ruby2-teachers-guide-mysql-setup)

+ **WHAT IS A DATABASE**
  * A relational database is essentially a series of tables that can be joined to one another.Each table is like an excel spreadsheet.
  *  A school may have a database with two tables one for students and another for grades. To link these two files, each student is assigned a unique identification number, which appears in both the personal information file and the grades file.

+ **SQL**
  * SQL is the language that controls databases (how you create and name tables, add information, add, delete, modify, and read information)
  * **Class should download Sequel Pro [here](http://www.sequelpro.com/)**

  I DONT KNOW HOW TO GET STUDENTS TO CONNECT TO THE DATABASE!!! _ NEED VANESSA

  * Creating a table:
  ```sql
    CREATE TABLE tweets (id integer auto_increment primary key, user VARCHAR(50), status VARCHAR(140)); 
  ```
    * `CREATE TABLE tweets`: We're actually creating the table in our databse called tweets
    * ` id integer auto_increment primary key`: Here we're creating the ID column, and the datatype of the information that will be stored in this table is an integer. `primary key` means it's a unique identifier for each row, and `auto_increment` means that for every new entry in the database, the ID will automatically increase by 1. 
    * `user VARCHAR(50)`: creating the user column with a string datatype. This can only hold 50 characters
    * `status VARCHAR(140)`: creating the status column which holds a string of 140 characters. VARCHAR stands for variable character.
  
  * Adding a row (adding data):
  ```sql
    INSERT INTO tweets (user, status) VALUES (“Danny”, “Hello world!”);
  ```
    * The ID column would get populated with 1 (happens automatically)
    * user column gets population with "Danny"
    * status column gets population with "Hello world!"

  * Read information:
  ```sql
    SELECT * FROM tweets 
  ```
    * `*` means we're selecting everything
    * `FROM tweets` means from the tweets table

  * Startup Sequel Pro
  I DONT KNOW HOW TO DO THIS!!!!

    * Under host put in teacher's IP address
    * Username and password are whatever the teacher creates
    * When you’ve established your connection you should see a dropdown menu in the top left corner where you can select a database - db created by teacher
    * have students enter their own information in the database
    * `select * from students` pulls all students
    * `select * from students where name="zach"` gives us one record if there is a match
    * `SELECT * FROM sunday_students WHERE favorite_food = "pizza"` gives all info about all students that like pizza
    * ``SELECT name FROM sunday_students WHERE favorite_food = "pizza"` gives us the names of the students who's fav food is pizza
    * SQL Challenges on board: https://github.com/flatiron-school-curriculum/hs-sql-queries-challenge 

+ **ACTIVE RECORD**
  ***Code snippets can be found [here](https://github.com/flatiron-school-curriculum/hs-week-3-code-snippets)***
  * SQL can be hard to write, especially when you're trying to pulll information from multiple tables.
  * ActiveRecord is gem that sets up a SQL databse and lets us write ruby code to read and write to the database
  * 




### Conclusion / So What?


### Hints and Hurdles