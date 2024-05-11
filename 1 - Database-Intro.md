# What is a Database

- Any collection of related information. Eg. - Phonebook, Shopping List, Todo List, Your 5 friends, Facebook's User Base

- Databases can be stored in various ways - on paper, in your mind, on a computer, powerpoint, comments section

- Computers are great at keeping track of large amouts of information

# Database Management Systems (DBMS)

- A special software that helps users create and maintain database.

  - Makes it easy to manage large amounts of information
  - handles security
  - backups
  - importing/exporting data
  - concurrency
  - interacts with software applications (programming languages)

- For eg, amazon.com will interact with DBMS in order to cread, read/retrieve, update and delete (C.R.U.D) information

# Types of DB

- ### Relational DB (SQL)
- ### Non-relational DB (noSQL)

### Relational DB

- organize data into one or more tables
  - each table has columns and rows
  - an unique key identifies each row

### Non-relational DB

- organize data in anything but a traditional table
  - key values stores
  - documents (JSON, XML, etc)
  - graphs
  - flexible tables

# Relational DB (SQL)

| \*ID | Name   | Major     |
| ---- | ------ | --------- |
| 1    | Jack   | Biology   |
| 2    | Kate   | Sociology |
| 3    | Claire | English   |
| 4    | John   | Chemistry |

| \*Username | Password | Email               |
| ---------- | -------- | ------------------- |
| jsmith22   | wordpass | someemail@email.com |
| catlover45 | apple223 | Sociology@email.com |
| gamerkid   | tiff62   | English@email.com   |
| giraffe    | africa   | Chemistry@email.com |

- Relational Database Management System (RDBMS)

  - Help users create and maintain a relational database
    - mySQL, Oracle, Postgres, MariaDB

- Structured Query Language (SQL)
  - Standardized language for interacting with RDBMS
  - Used to perform C.R.U.D operations as well as other administrative tasks (user management, security, backup etc)
  - Used to define table and structures
  - SQL Code used on one RDBMS is not always portable to another without modification.

# Non-relational DB (noSQL)

```db
[
  {
    "_id": 1,
    "name": "Jack",
    "major": "Biology"
  },
  {
    "_id": 2,
    "name": "Kate",
    "major": "Sociology"
  },
  {
    "_id": 3,
    "name": "Clare",
    "major": "English"
  },
  {
    "_id": 4,
    "name": "John",
    "major": "Chemistry"
  },
]
```

- Non-relational database management system (NDBMS)

  - help users create and maintain a non-relational database
    - mongoDB, dynamoDB, Cassandra, Firebase, ScyllaDB

- Implementation specific

  - Any non-relational database falls under this category, so there is no set language standard
  - Most NRDBMS will implement their own language for performing C.R.U.D and administrative operations on the database.

# Database Queries

- Queries are requests made to the database management system for specific information.

- As the database's structure becomes more and more complex, it becomes more difficult to get the specific pieces of information we want.

- A google search is a query.

# Section Wrap Up

- Database is any collection of related information.

- Computers are great for storing databases.

- Database Management System (DBMS) make it easy to create, maintain and secure a database.

- DBMS allow you to perform the C.R.U.D operations and other administrative tasks

- Two types of database: Relational & Non-relational

- Relational databases use SQL and store data in tables with rows and columns

- Non-relational store data using other data structures
