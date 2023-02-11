# Week 3

### Weekly Aims:
1. Learn how to setup PostgreSQL and use SQL to read and manipulate data stored in an existing database. **✓**
2. Learn how to setup and gradually build a program which communicates with a database. **✓**
3. Learn how to design schemas using either one or two related tables from a plain English specification. **✓**
4. Learn to test-drive "Repository" class methods. **✓**
5. Learn to design Repository classes using one-to-many & many-to-many relationships. **✓**

---
### Weekly Objectives:
1. Use SQL to query a database to read data from one table or resulting of a join, create new records, update and delete.
2. Integrate a relational database to a program by test-driving classes which implement CRUD methods to send SQL queries to a database.
3. Design a database schema with at least two tables from a specification, including a one-to-many relationship between two tables, and create the schema in a database using SQL.
5. Explain how a program communicates with its database by creating a sequence diagram.
6. Develop a small terminal program that allows users to manage a shop database containing some items and orders.

---
### Evidence

#### Main Project - Shop Manager System
[Link here](https://github.com/forreya/shop-database-manager). Skills practiced & challenges faced:
1. Involved writing a small terminal program that allows users to manage a shop's database containing some items and orders.
2. Integrates the shop's database to 'app.rb' by using the PG gem, and through test-driven Repository classes.
3. Used more advanced SQL database techniques such as 'joins' & implementing many-to-many table relationships. 

#### 1. Settng up PostgreSQL and use SQL to read and manipulate data stored in an existing database
- **Installed PostgreSQL on my laptop** using Homebrew.
- **Learned how to use the built-in REPL, psql,** that can be used to directly type-in SQL to interact with databases.
- **Learned how to import seeds, create databases, and to send SQL queries to databases**
- **Started using TablePlus**, a graphical interface for navigating and interacting with databases.

Evidence of these bullet points are difficult to show as the databases I created and tinkered with are stored on my MacBook.

#### 2. Setting up and building programs that communicates with databases
*Throughout the week, I setup multiple programs that communicates with databases.*

**All** these projects used these components:

* **Ruby and RSpec**  
  The programming language and test framework.
* **The `pg` gem**  
  A library that allows the program to send SQL queries to the database, and retrieve the result set.
* **A class `DatabaseConnection`**  
  A class that acts as a thin layer with methods to connect to PostgreSQL and send SQL queries to it.

Some examples of mini-programs I worked on can be found [here](https://github.com/forreya/SQL-database-projects/tree/main/mini-projects). These projects/challenges range from simple programs containing only one table, to programs that have multiple tables with many-to-many relationships.

#### 3. Designing schemas using either one or two related tables from a plain English specification.
I designed a great number of table recipes based on various user stories. I began with simple one-table schemas, then moved on to creating schemas with two tables and a foreign key, to finally designing schemas for two related tables with a many-to-Mmany relationship.

You can find evidence of this [here](https://github.com/forreya/SQL-database-projects/tree/main/designing-schema).

#### 4. Test-driving "Repository" class methods.
- **Test drove a recipes databasing system that implemented 'all' and 'find' repository class methods**. The system keeps a list of food recipes, including information like average cooking time & rating. For this challenge, I had to create a database named 'recipes_directory' & another test database 'recipes_directory_test' for testing. The full recipe databasing system can be found [here](https://github.com/forreya/SQL-database-projects/tree/main/mini-projects/recipes-directory).
- **Test drove a social network system that implemented the four methods all, find, create, delete & update for each Repository class.** [This video folder](https://github.com/forreya/makers-portfolio/tree/main/videos/social-network) contains a 3 videos of me developing this system from scratch (designing, test-driving, debugging, etc).

#### 5. Designing repository classes using one-to-many & many-to-many relationships.
- **I made a [sequence diagram](https://github.com/forreya/makers-portfolio/blob/main/videos/sequence-diagram.mp4)** using *diagram.codes* and explained the detailed flow of a [book store system](https://github.com/forreya/SQL-database-projects/tree/main/mini-projects/book-store) that uses PostgreSQL to store, update, delete & display information on various books. 
- **I designed & test drove a music library system** that uses PostgreSQL to store, update, delete & display data on various albums & artists. The code, tests, seeds, and recipes for this database program can be found [here](https://github.com/forreya/music-library).

In addition to this, most of the projects that have already been linked, including my [shop databasing manager](https://github.com/forreya/shop-database-manager) project all involved designing simple-to-complex repository classes and I had loads of practice developing these types of class methods throughout the week.

---
### Daily Journal/Notes

#### Day 1:
Installed `PostgreSQL` using the given [instructions](https://github.com/makersacademy/databases/blob/main/sql_bites/01_setting_up_database.md). Some random facts about 'psql':
- Exit psql using \p
- The -h option specifies the IP address of the machine PostgreSQL runs on. Use 127.0.0.1 for the local IP address of my machine, on which PostgreSQL runs.
Also learnt to use TablePlus & learned object-relational mapping.

#### Day 2:
Today I restructured my github repos to have one big repo for all my SQL challenges (book-store, recipes-directory). I pair programmed with my friend Terry (@terryhycheng). Learnt about a better database GUI alternative to TablePlus- Beekeeper Studio (Community Edition). It doesn't keep prompting you to buy the full version all the time.

#### Day 3:
Finished my [social network databasing system](https://github.com/forreya/SQL-database-projects/tree/main/mini-projects/social-network).

#### Day 4:
Learnt about Struct in Ruby. Struct is a built-in Ruby class, it’s used to create new classes which produce value objects. A value object is used to store related attributes together. It acts a little like a normal custom user-created class, but provides some nice default functionality and shortcuts when you don't need a full-fledged class. More detail on Structs can be found [here](https://www.rubyguides.com/2017/06/ruby-struct-and-openstruct/).

---
### End-of-Week Evaluation
*Were all the weekly aims achieved?*



*Were there any roadblocks/difficulties you had to face?*


---