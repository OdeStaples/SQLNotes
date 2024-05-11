Student Table

`Note: Primary keys have a `\*`before them while foreign keys have a`\*` after them and composite keys have`\*\*` before them`

| \*student id | Name   | Major        |
| ------------ | ------ | ------------ |
| 1            | Jack   | Biology      |
| 2            | Kate   | Sociology    |
| 3            | Claire | English      |
| 4            | John   | Chemistry    |
| 5            | Mike   | Comp Science |

- All tables in Relational DB are going to have rows and columns.
- Columns define a single attribute, for eg. names columns are going to contain student names.

- A row is an indivisual entry in the table, for eg. in the student table, each row represents a single student.

- In relational databases, there is going to be a special column called the
  primary key. Primary key is an attribute that uniqely defines a row in the database.

- Primary keys are useful for differentiating between the entries in the db, for eg - in the above table, there are two students with same name and major
  but since their primary keys are different, we'll be able to differentiate between the two rows.

- A primary key can be a number or string or any type but it must be able to uniquely identify the row

User Table

| \*email             | password | date_created | type    |
| ------------------- | -------- | ------------ | ------- |
| fake@email.com      | Jack     | 1-1-1995     | Admin   |
| fake123@email.com   | Kate     | 2-2-1995     | Free    |
| fake111@email.com   | Claire   | 3-3-1995     | Free    |
| emailfake@email.com | John     | 4-4-1995     | Premium |
| test@email.com      | Mike     | 5-5-1995     | Free    |

- In the User table, the email is the primary key which is unique to each entry

# Types of Primary Keys

- There are two types of primary keys;

  - Surrogate Key
  - Natural Key

  ### Surrogate Key

  - A surrogate key is a type of primary key that has no mapping to anything in the real world.

  - In the below table, the empid has no mapping in the real world

  User Table

  | \*emp_id | name   | birth_date | sex | salary |
  | -------- | ------ | ---------- | --- | ------ |
  | 100      | Jack   | 1-1-1995   | M   | 100    |
  | 101      | Kate   | 2-2-1995   | F   | 200    |
  | 102      | Claire | 3-3-1995   | F   | 300    |
  | 103      | John   | 4-4-1995   | M   | 400    |
  | 104      | Mike   | 5-5-1995   | M   | 500    |

  ### Natural Key

  - A natural key is a type of primary key that serves a purpose in the real world and not just in the database only.

  - In the below table, the aadhar number has real world implications

  Employee Table

  | \*emp_aadhar | name   | birth_date | sex | salary |
  | ------------ | ------ | ---------- | --- | ------ |
  | 100          | Jack   | 1-1-1995   | M   | 100    |
  | 101          | Kate   | 2-2-1995   | F   | 200    |
  | 102          | Claire | 3-3-1995   | F   | 300    |
  | 103          | John   | 4-4-1995   | M   | 400    |
  | 104          | Mike   | 5-5-1995   | M   | 500    |

# Foreign Key

- It is an attribute that we can store on a database table that can link us to another database table.

- In the below example in the employee, the foreign key is the branch_id which in turn is a primary key(`branch_id`) in the branch table.

- In the branch table, the `mgr_id` is a foreign key which is a primary key (`emp_id`) in the employee table.

Employee Table

| \*emp_id | name   | birth_date | sex | salary | branch_id\* |
| -------- | ------ | ---------- | --- | ------ | ----------- |
| 100      | Jack   | 1-1-1995   | M   | 100    | 1           |
| 101      | Kate   | 2-2-1995   | F   | 200    | 2           |
| 102      | Claire | 3-3-1995   | F   | 300    | 3           |
| 103      | John   | 4-4-1995   | M   | 400    | 2           |
| 104      | Mike   | 5-5-1995   | M   | 500    | 3           |

Branch Table

| \*branch id | branch_name | mgr_id\* |
| ----------- | ----------- | -------- |
| 1           | Corporate   | 101      |
| 2           | Scranton    | 102      |
| 3           | Stanford    | 103      |

### Do foreign keys always link to primary keys in another table

    - No, foreign keys do not always link to primary keys. A foreign key can refer to a unique key or a primary key of the parent table. However, standard SQL recommends that a foreign key's reference should be a unique key or the primary key in the referenced table. If the foreign key refers to a non-primary unique key, the column names of the key must be explicitly specified.

- Foreign keys help us define relationships between tables.

- A table can have multiple foreign keys. For eg, in the below table, the `branch_id` and `super_id` are foreign keys:

  | \*emp_id | name   | birth_date | sex | salary | branch_id\* | super_id\* |
  | -------- | ------ | ---------- | --- | ------ | ----------- | ---------- |
  | 100      | Jack   | 1-1-1995   | M   | 100    | 1           | NULL       |
  | 101      | Kate   | 2-2-1995   | F   | 200    | 2           | 100        |
  | 102      | Claire | 3-3-1995   | F   | 300    | 3           | 100        |
  | 103      | John   | 4-4-1995   | M   | 400    | 2           | 101        |
  | 104      | Mike   | 5-5-1995   | M   | 500    | 3           | 101        |

# Composite Keys

- A composite key in SQL is a combination of two or more columns that uniquely identify each row in a table. A single column can't identify a row uniquely, but a combination of columns can.

- For eg, in the below branch supplier table, the `branch_id` and `supplier name` are composite keys and the combination of such keys only exist once - Hammer Mill supplies to Branch Id 2: this combination only occurs once.

  Employee Table

| \*emp_id | name   | birth_date | sex | salary | branch_id\* |
| -------- | ------ | ---------- | --- | ------ | ----------- |
| 100      | Jack   | 1-1-1995   | M   | 100    | 1           |
| 101      | Kate   | 2-2-1995   | F   | 200    | 2           |
| 102      | Claire | 3-3-1995   | F   | 300    | 3           |
| 103      | John   | 4-4-1995   | M   | 400    | 2           |
| 104      | Mike   | 5-5-1995   | M   | 500    | 3           |

Branch Table

| \*branch id | branch_name | mgr_id\* |
| ----------- | ----------- | -------- |
| 1           | Corporate   | 101      |
| 2           | Scranton    | 102      |
| 3           | Stanford    | 103      |

Supplier Table

| \*\*branch id | \*\*supplier_name   | supply_type      |
| ------------- | ------------------- | ---------------- |
| 2             | Hammer Mill         | Paper            |
| 2             | Uni-ball            | Writing Utensils |
| 3             | Patroit Paper       | Paper            |
| 2             | J.T. Forms & Labels | Custom Forms     |
| 3             | Uni-ball            | Writing Utensils |
| 3             | Hammer Mill         | Paper            |
| 3             | Samford Labels      | Custom Forms     |
