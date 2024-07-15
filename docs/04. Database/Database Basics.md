> A **database** is an organized collection of structured information or data. Databases are managed by **Database Management Systems (DBMS)**, a software that provides an interface for users and applications to create, retrieve, update, and delete data efficiently and securely.

## Database Management System (DBMS)
DBMS is a special software program that helps users create and maintain a database on a computer. It   
- makes it easy to manage large amounts of information
- handles security 
- does backups
- import/export data
- concurrency
- interacts with other software applications

The database management system is not the actual database, it is the software application that is creating, maintaining, updating, and deleting information from the actual database. 
### Types of Databases
#### 1. Relational Databases (SQL)
Organize data into more or more tables. 
- Each table has columns and rows. 
- A **unique** key identifies each row, e.g., `id`, `username`.

Popular **Relational Database Management Systems (RDBMS)** are ***PostgreSQL, MySQL, MariaDB, Oracle, etc.*** 

Relational database management systems use **Structured Query Language (SQL)**. 
- A standardized language for interacting with RDBMS. 
- It’s used to perform **C.R.U.D. operations** and **administrative tasks** (user management, security, backup, etc). 
- It’s used to define tables and structures. 
- SQL code used on one RDBMS is not always portable to another without modification. 

![](https://i.imgur.com/D2Dw6ou.png)
#### 2. Non-Relational (no SQL / not just SQL)
Organize data in anything but a traditional table. 
- Key-value stores
- Documents (JSON, XML, etc.)
- Graphs
- Flexible Tables

Popular **Non-Relational Database Management Systems (NRDBMS)** are **MongoDB, dynamoDB, firebase,** etc. 

- Any non-relational database falls under this category, so there’s no set language standard. 
- Most NRDBMS will implement their language for performing C.R.U.D and administrative operations on the database. 
#### 3. Database Queries
Queries are requests made to the database management system for specific information. 
As the database’s structure becomes more and more complex, it becomes more difficult to get the specific pieces of information we want. 
→ We can write a complex database query, instructing the DBMS to grab specific information from the database.
## Database Tables
![](https://i.imgur.com/eY0TI1I.png)

- A column would define a single attribute, a row is an individual entry in the student table. 
- When creating a table in the database, we want to create a **primary key attribute** (`student_id`). A primary key is **unique** for each row in the table → defines the rows in the database **uniquely**. 