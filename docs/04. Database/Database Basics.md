> A **database** is an organized collection of structured information or data, typically stored and accessed electronically. Databases are managed by **Database Management Systems (DBMS)**, a software that provides an interface for users and applications to create, retrieve, update, and delete data efficiently and securely.

## Database Management System (DBMS)
A **Database Management System** (DBMS) is specialized software that facilitates the creation, maintenance, and use of electronic databases. It   
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
- A standardized language for managing and manipulating relational databases. 
- It’s used to perform **C.R.U.D. operations** and **administrative tasks** (user management, security, backup, etc). 
- It’s used to define tables and structures. 
- SQL code used on one RDBMS is not always portable to another without modification. 

![](https://i.imgur.com/D2Dw6ou.png)
#### 2. Non-Relational (no SQL / not just SQL)
Non-relational databases (NoSQL databases) organize data using flexible schemas that differ from the traditional table-based structure of relational databases. 
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

A column would define a single attribute, a row is an individual entry in the student table. 
### 1. Primary Key
When creating a table in the database, we want to create a **primary key attribute** (`student_id`). A **primary key** is a column or set of columns that uniquely identifies each row in a table, ensuring data integrity and providing a means for establishing relationships between tables.

In database design, the terms **surrogate key** and **natural key** also refer to types of primary keys.
- A **surrogate key** is an artificial key that is not derived from the application data. It is typically a sequential number (like an auto-incremented integer). It has **no** **meaning** or intrinsic value **outside the database** context. → simple, stable, and guarantees uniqueness.
- A **natural key** is a key that is derived **from the actual data**. It often comes from the business logic, like a Social Security Number (SSN), email address, or a combination of fields → can sometimes be problematic if the business logic/data changes.
### 2. Foreign Key
A **foreign key** is a column or set of columns in one table that refers to the primary key in another table, establishing a link between the two tables.

<u>**Example 1**</u>: 
![](https://i.imgur.com/wAmG5FV.png)
A company can have different branches, and we can store information about an employee’s branch using a foreign key. 
- Within the `employees` table, we have a foreign key `branch_id`. `branch_id` is the primary key of the `branches` table. 
![300](https://i.imgur.com/6IiuJCc.png)
- Now, we will know which branch an employee belongs to without storing branch information on the `employees` table. 

A table can **have more than one foreign key** on it. 

<u>**Example 2:** </u>
Here, the `employees` table has two foreign keys: 
- `branch_id`, which points to the `branches` table 
- `super_id`, which defines the supervisor of a particular employee and points back to the `employees` table (the same table)
→ using the `super_id`, we can define the relationship between employees 
![](https://i.imgur.com/B7qKuoU.png)
### 3. Composite Key