## 1. What is a DBMS? Differentiate between DBMS, RDBMS.
Relational Database Management System is an advanced version of a DBMS. 
- DBMS Database management system, as the name suggests, is a management system that is used to manage the entire flow of data, i.e, the insertion of data or the retrieval of data, how the data is inserted into the database, or how fast the data should be retrieved, so DBMS takes care of all these features, as it maintains the uniformity of the database as well does the faster insertions as well as retrievals. Mongo DB, Cassandra are some popular examples of DBMS

- Relational Database Management System (RDBMS) is a more advanced version of a DBMS system that allows access to data in a more efficient way. It is used to store or manage only the data that are in the form of tables.
MySQL, Oracle Database, Microsoft SQL Server are the most common examples of RDBMS
## 2. What is normalization? Explain the different normal forms.
- Normalization is the process of organizing data in a database to **reduce redundancy** and improve data integrity. 
- It involves dividing a database into two or more tables and defining relationships between the tables.
- When we normalize tables, we break them into multiple smaller tables. 


    - First Normal Form (1NF): Ensures that the database table is organized such that each column contains atomic (indivisible) values, and each record is unique. 
    - Second Normal Form (2NF):  2NF eliminates redundant data by requiring that each non-key attribute be dependent on the primary key. This means that each column should be directly related to the primary key, and not to other columns.
    - Third Normal Form (3NF):Meet all the requirements of the 2NF. Additionally, remove columns that are not dependent on the primary key.
    - Boyce-Codd Normal Form (BCNF):BCNF is a stricter form of 3NF that ensures that each determinant in a table is a candidate key. In other words, BCNF ensures that each non-key attribute is dependent only on the candidate key.
    - Fourth Normal Form (4NF): 4NF is a further refinement of BCNF that ensures that a table does not contain any multi-valued dependencies.
    - Fifth Normal Form (5NF): 5NF is the highest level of normalization and involves decomposing a table into smaller tables to remove data redundancy and improve data integrity.
## 3. What is denormalization? When and why would you denormalize a database?
When we normalize tables, we break them into multiple smaller tables. So when we want to retrieve data from multiple tables, we need to perform some kind of join operation on them. In that case, we use the denormalization technique that eliminates the drawback of normalization.


Denormalization is the process of combining tables to reduce the complexity of joins and improve query performance. 

**Real-world analogy**\
Imagine a fruit seller has two daily lists: one of in-stock fruit and another with the market prices of all fruits and vegetables. In a normalized database, these lists would be two separate tables. If a customer wanted to know an item's price, the seller would check both lists to determine if it is in stock and at what price. The process would be slow and annoy the customer.

As an alternative, the seller creates another list every morning with just the in-stock items and the daily price of each item. Combining the two lists provides a single reference that can be used to quickly generate answers. This is a type of database denormalization.

## 4. What is a database key? Can a table have multiple primary keys?
####  A. Primary Key
- The primary key refers to a column/key or a set of columns/keys of a table that helps us identify all the records/tuple uniquely present in that table. 
- Not null
#### B. Candidate key
- The minimal set of attributes that can uniquely identify a tuple is known as a candidate key.
- Support null
- Minimal super key
#### C. Alternate Key
- An alternate key is a candidate key that is not chosen as the primary key. These are potential unique identifiers.
- Non-null
#### D. Composite Key
- Sometimes, a table might not have a single column/attribute that uniquely identifies all the records of a table. To uniquely identify rows of a table, a combination of two or more columns/attributes can be used. 
- Not Null
#### E. Foreign Key (FK)
- Foreign keys are the column of the table used to point to the primary key of another table.
#### F. Super Key
- A super key is a set of one or more columns that can uniquely identify rows in a table.
- Any candidate key is also a super key, but not all super keys are candidate keys.
#### F. Unique Key
- A unique key is a database concept used to identify and distinguish individual records within a table.
- All specified columns must be unique, not necessarily each column individually
- Support null values.
- Can be created using multiple column.

## 5. Explain ACID properties in the context of database transactions.
Properties of a transaction are the ACID properties.
The ACID properties in Database Management Systems (DBMS) are crucial to ensuring the reliability and integrity of data. 
### Atomicity
Atomicity - each statement in a transaction (to read, write, update or delete data) is treated as a single unit. Either the entire statement is executed, or none of it is executed. If any part of the transaction fails, the entire transaction is rolled back, leaving the database in its original state.
- Bank money transaction system. Send money and get money should be in single unit.
### Consistency
DBMS ensures that any transaction made is valid according to all defined rules and does not violate any constraints in the database system.
- Databases often have rules (constraints) to ensure data integrity. These rules might include:
    - Primary Key Constraints: Ensuring that each record has a unique identifier.
    - Foreign Key Constraints: Ensuring that a value in one table corresponds to a valid record in another table.
### Isolation
This property of ACID ensures that concurrent transactions do not interfere with each other and that all operations in a transaction are treated as if they were executed sequentially. This means if multiple transactions occur simultaneously, each transaction completes separately and does not affect the other transactions. It also ensures that any changes made by a transaction are permanent and are not affected by other transactions.
### Durability
This property ensures that once the transaction has completed execution, the updates and modifications to the database are stored in and written to disk and they persist even if a system failure occurs. These updates now become permanent and are stored in non-volatile memory. The effects of the transaction, thus, are never lost. 


## 6. What is a transaction? Explain the properties of a transaction.
- A transaction is a unit of work performed within a database management system. It is treated in a coherent and reliable way independent of other transactions.
- Properties of a transaction are the ACID properties (Atomicity, Consistency, Isolation, Durability).
## 7. What is a deadlock? How can it be avoided in DBMS?
A deadlock is a situation where a set of processes are blocked because each process is holding a resource and waiting for another resource acquired by some other process. 
- Avoiding deadlocks:
    - Implementing a timeout for transactions.
    - Using a deadlock detection algorithm
    - Avoiding cyclic dependencies

## 8. What is a view? How is it different from a table?
The main difference between them is that a 
-  table is an object that consists of rows and columns to store and retrieve data whenever the user needs it. 
- In contrast, the view is a virtual table based on an SQL statement's result set and will disappear when the current session is closed. 
## 9. What is a trigger? How does it work in a database?
A trigger is a database object that automatically executes a specified set of SQL statements when a certain event occurs on a table or view, such as an insert, update, or delete operation.    
- How it works:
    - Triggers are associated with a table or a view.
    - When a specified event occurs, the trigger is activated.
    - The trigger executes the SQL statements defined in it automatically.
## 10. Explain the difference between a clustered and a non-clustered index.
- Clustered Index: 
Analogy: Think of a clustered index like a phone book where the names are sorted alphabetically. The entries are physically organized in the book by last name, so if you want to find "John Doe," you can quickly flip to the section with last names starting with "D."

Definition: A clustered index is used to define the order or to sort the table or arrange the data by alphabetical order just like a dictionary.

- Non-Clustered Index: 
Analogy: Think of a non-clustered index like an index at the back of a textbook. The index lists topics and subtopics along with page numbers where the actual content can be found. The book's content isn't stored in the order of the index, but the index helps you quickly find where the information is.

Definition: A non-clustered index creates a separate structure that stores the index key values and pointers (row locators) to the actual data rows.

## 11. What is the difference between a delete and truncate statement in SQL?
- DELETE:
    - The DELETE command is used to delete specified rows(one or more) based on a WHERE condition.
    - Can be rolled back.
- Truncate
    - While this command is used to delete all the rows from a table.
    - Cannot be rolled back in many DBMS

## 12. What are the different types of joins in SQL? Explain with examples.
- Inner Join: Returns records that have matching values in both tables
- Left Join (Left Outer Join): Returns all records from the left table, and the matched records from the right table. Returns NULL for unmatched right table records.
- Right Join (Right Outer Join): Returns all records from the right table, and the matched records from the left table. Returns NULL for unmatched left table records.
- Full Join (Full Outer Join): Returns all records when there is a match in either left or right table records.

## 13. What is the purpose of the GROUP BY clause in SQL?
In SQL, The Group By statement is used for organizing similar data into groups. 

The GROUP BY statement is often used with aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG()) to group the result-set by one or more columns.

## 14. What is the purpose of the HAVING clause in SQL?
The HAVING clause is used to filter groups based on a specified condition. It is similar to the WHERE clause but is used for groups.

After use group by then use having.

## 15. What is the difference between the WHERE and HAVING clauses in SQL?
- WHERE:
    - Used to filter records before any groupings are made.
    - Cannot be used with aggregate functions.
- HAVING:
    - Used to filter groups after the GROUP BY clause.
    - Can be used with aggregate functions.

## 16. Explain the concept of data integrity in DBMS.
Data Integrity ensures the accuracy, consistency, and reliability of data stored in a database.
## 17. What are the different types of relationships that can exist between tables?
- One-to-One (1:1): Each row in Table A is linked to one and only one row in Table B, and vice versa.
- One-to-Many (1): Each row in Table A can be linked to one or more rows in Table B, but each row in Table B is linked to only one row in Table A.
- Many-to-Many (M): Each row in Table A can be linked to multiple rows in Table B and vice versa. This is usually implemented with a junction table.
## 18. What is the purpose of the COMMIT and ROLLBACK statements in SQL?
- COMMIT: Saves all changes made during the current transaction and makes them permanent.
- ROLLBACK: The ROLLBACK statement lets a user undo all the alterations and changes that occurred on the current transaction after the last COMMIT.
## 19. Explain the difference between a logical and a physical data model.
- These high-level, abstract representation of data emphasizes structure and relationships without focusing on physical implementation details. 
- Physical data model. These detailed, tangible representations of data describe how it will be stored, accessed, and retrieved within a database system. 

## 20. Authentication vs authorization
- Authentication is about proving who you are.
    - Examples:
        - Entering your PIN at an ATM.
        - Logging into your email with a password.
        - Scanning your fingerprint to unlock your phone.

- Authorization is about what you can do and what you can access after you have been authenticated.
    - Examples:
        - After logging into your email, you can read and send emails but not access the email server settings.


In a simple term.
- Authentication: Proves your identity. (e.g., logging in)
- Authorization: Grants or denies permission to access resources. (e.g., accessing specific files or features)