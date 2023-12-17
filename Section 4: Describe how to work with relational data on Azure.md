# Characteristics of Relational Data

- Table: Data is stored in a table
- Table consist of rows and columns
- Row: each row repersents a single instance of an entity
- Column: define the properties of the entity
- Each column is defined by a datatype
- All rows have the same number of columns

<br>

- Some columns are used to maintain relationships between tables
- Model shows the structure of the entities
- Primary Key: uniquely identify each row
- Foreign Key: reference, or link to, the primary key of another table
  - used to maintain the relationships between tables

<br>

## Normalization

Split an entity into more than one table <br>

- Reduce storage
- Avoid data duplication
- Improve data quality

<br>

## Structured Query Language (SQL)

- Most relational databases support Structured Query Language (SQL)
  - SQL Server - TSQL
  - Oracle - PL/SQL
- You use SQL to create tables, insert, update, and delete rows in tables, and to query data

<br>

## Realational database use cases

- Relational databases are well suited for OLTP applications
- OLTP applications are focused on transaction-oriented tasks that process a very large number of transactions per minute
- Examples of OLTP applications that use relational databases are
  - Banking solutions
  - Online retail applications
  - Flight reservations systems
  - Most online purchasing applications
- Relational Database NOT use for
  - Music, video, or other media files - Blob storage
  - Social networking sites, highly complex web of relationships - Graph Database

<br>

## Benefits of Relational Database

- Consistency: Maintains data consistency across applications and database queries
- Commitment and Atomicity: Handles business rules and policies at a very granular level with strict policies
- Locking and COncurrency: Prevents other users and applications from accessing data while being updated

<br>

## Main characteristics of a relational database are:

- All data is tablular. Entities are modeled as tables, each instance of an entity is a row in the table, and each property is defined as a column
- All rows in the same table have the same set of columns
- A table can contain any number of rows
- A primary key uniquely identifies each row in a table. No two rows can share the same primary key
- A foreign key references rows in another, related table. For each value in the foreign key column, there should be a row with the same value in the corresponding primary key column in the other table

<br>

# Relational Data Structure

## Non-clustered Index - Good or Bad

- Non-cluster Indexes consume additional storage space
- Each time you insert, update, or delete data in a table, the indexes for that table must be maintained
- Recommendations
  - Read only table - more indexes will improve query performance
  - Transaction table - more indexes on that table can slow your system down
  - You must strike a balance between having indexes that speeds up your queries versus the cost performing other operations

<br>

## What is a View

- View is a virtual table based on the result set of a query
  - View does not store data but very much behave like a table
  - You can query view like a table
- A view can combine data from two or more tables, using joins, and also just contain a subset of information. This makes them convenient to abstract, or hide complicated queries.

<br>
<br>

# Provisioning and Deployment

## What is provisioning and deployment

- Provisioning and deployment means to execute series of steps to create and configure a service
  - We need to provide parameters that provides a estimate of the size of the workload that we want to run
  - Behind the scenes Azure will create other required resources: Disks, memory, CPUs, network and so on
  - You will be charged for these resources until you delete them
  - We can scale dynamically 
