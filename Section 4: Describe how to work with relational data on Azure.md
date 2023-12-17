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
