# ST207 - DATABASES: Assignment 2 (MT2022)

### Overall objective

This assignment is intended to assess your knowledge about **database programming techniques**, more specifically how to incorporate SQL DDL and DML commands into a programming language through a **library of functions**.

### Instructions

1. Choose a database application of your interest. Section Examples brings some ideas that you can use and complement, but feel free to choose any other database application.

2. Write a *miniworld* description of your chosen application. This can be a small database application (e.g. up to 8 entities) for which you can clearly describe: i) all the entities and their attributes, ii) all the relationships among entities, and iii) all the constraints at the application level/business rules (e.g. an employee's salary cannot be zero or bigger than her/his supervisor's salary). Your miniworld description can be a set of paragraphs stating these three items listed above. You **don't need** to draw any conceptual model or E-R diagram (this is optional).

3. Write a Python program (notebook) making use of the `sqlite3` library. This is your minimal requirement. Alternatively, you can use the `sqlalchemy` or `peewee` libraries instead of `sqlite3`. Your program must:

* import all the necessary libraries and establish a database connection.
* create all the necessary tables, via DDL commands. Alternatively, you can load your data from CSV or any other file format (e.g. JSON) into Pandas dataframes (or other Python data structures).
* verify that all primary key, foreign key, and `NOT NULL` constraints are checked - this should be automatically checked by the database system, but make sure your commands are correct and providing all necessary data.
* create at least one (or more) `VIEW` tables with all the necessary attributes. You must write a paragraph in your Python notebook justifying i) why each view is needed in the context of your chosen application, and ii) what attributes are part of each view. Remember that the view can be use as any other database in your system, which means you can use it in `JOIN`, `IN`, and any other operation. Also, it's up to you to decide whether each view will be temporary or permanent.
* specify a list of `TRIGGER` commands to be checked against any DML command changing the database state (i.e., inserting, updating, and deleting data). You **don't need** to use all types of triggers, but make sure you have covered a comprehensive list of operations that can modify your database and that your triggers will be able to ensure the consistency (including constraints violation) of your database application.

4. For testing your database application, make sure you have a consistent set of DML commands (e.g. INSERT, UPDATE, DELETE, and SELECT). You must specify at least 5 (five) SQL queries involving multiple tables (you can use `JOIN` or subqueries), aggregation functions, and `GROUP BY` directives. When defining your queries, think on the most probable information a given user would need to retrieve for your database and then write your SQL commands to answer them. Make sure you describe all SQL questions with the appropriate level of detail, so a layman person can understand what you are trying to retrieve from the database.

5. [this is optional] Feel free to use the `datapane` library (discussed in Week2) or any other graphical format for presenting your query results. The minimal requirement is for presenting these results in your Python notebook.

6. Upload your Python notebook and any other additional files (e.g. CSV files with your input data, graphical files with your query results) to GitHub. Make sure you **don't have any specific file path** - e.g. access to your Google Drive or other - preventing the access to your application's data.

### Examples of database applications

* database for elections, capturing data on parties, candidates, voters, votes and results.
* database to keep track of the teams (including coaches), referees, and games of a sports league.
* a banking database, capturing data on branches, customers, accounts, loans, and investments.
* a conference review database, capturing data on authors (researchers), reviewers, papers, conference, and written reviews.
* database for a library, keeping track of users/customers, collection (books, DVD, CD) and their respective authors, loans, and fines.
* database for an art museum, comprising data on art objects (that can be sculptures, paintings, statues or other types), artists, and exhibitions. Art objects can be also categorised as permanent collection or borrowed from other places, which requires the database to keep track of the object owner's data, loan period and cost.
* database for a hotel network, capturing data on hotels, employees, bookings, and guests/customers. Observe that a booking can be transformed into a real reservation (stay at the hotel) once the guests are checked-in in the hotel.

### Important dates

* Assignment released: 25/11/2022
* Submission of solution: 09/12/2022
* Feedback and grade (provisional): 23/12/2022

### Marking criteria

* This assignment is worth 20% of the final grade.
* **IMPORTANT**: according to the School policy, you **must** submit an answer to this assignment; otherwise, you will be graded 0 (zero).

| Problem breakdown  | Max marks | Your marks |
| ------------- | ------------- | ------------- |
| 2.i - Description of entities and attributes  | 5 | 5 |
| 2.ii - Description and correct mapping of all relationships  | 10 | 10 |
| 2.iii - Description and correct mapping of constraints related to business rules | 10 | 10 |
| 3.i - Choice of library and database connection | 5 | 5 |
| 3.ii/3.iii - Table creation and data loading, including relational constraints check (`PK`, `FK`, `NOT NULL`) | 15 | 15 |
| 3.iv - `VIEW` definition and implementation | 10 | 10 |
| 3.v - `TRIGGER` definition and implementation | 15 | 15 |
| 4 - SQL commands  | 30 | 30 |
| TOTAL  | 100 | 100 |
