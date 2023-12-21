# Introduction to NoSQL

## RDBMS were lacking

- Scalability
- Flexibility

<br>

## What is NoSQL

"Not Only SQL" or no structure query language

- Scalability: Horizontal scaling is possible
- Flexibility: No schema enforced

<br>

### Vertical Scaling

- Add more CPU, RAM, HDD in the same system

### Horizontal Scaling

- Add more commodity machines in a system

<br>

## NoSQL Use Cases

- Big data and real-time web applications
- Relationship between data is not important
- Data change frequently

<br>

## NoSQL Limitations

- Schema-less data means inconsistent data
- Denormalized data means redundant data
- Redundant data means inaccuracies and conflicts
- Dose not support many good features of Relational DB
  - Examples: Stored procedures, views, row level security, locks, etc.

<br>
<br>

# SQL vs NoSQL

## SQL

- Relational database
- Fixed schema
- Designed for complex queries
- SQL, MySQL, Oracle, Postgres
- Vertical scaling
- Row Oriented
- Tables
- Limited for big data

<br>

## NoSQL

- Non-relational or distributed
- Dynamic
- Not for complex queries
- MongoDB, Redis, Hbase
- Horizontal scaling
- Multi-model oriented
- Collections
- Great for big data

<br>
<br>

# 4 Types of NoSQL Databases

### Document
### Graph
### Key-Value
### Wide-Column

<br>

## Key-Value Store

- Uses a simple key/value to store data
- Quick to query due to its simplicity
- Value can be JSON, BLOB, String etc.
- <b>Use Cases:</b>
  - User profiles and session info on a website, blog comments, telecom directories, IP forwarding tables, shopping cart contents on e-commerce sites and more
- <b>Examples:</b>
  - Cosmos DB Table API, Redis, Table Storage, Oracle NoSQL Database, Voldemorte, Aerospike, Oracle Berkeley DB

<br>

## Document Store

- Document-oriented model to store data
- Similiar to key/value store, difference is that, the value in a document store database consists of semi-structured data
- Each record and its associated data within a single document
- Document stores are usually XML, JSON, BSON, YAML, etc
- <b>Use Cases:</b>
  - Content management systems, blogging platforms, and other web applications, blog comments, chat sessions, tweets, ratings, etc.
- <b>Examples:</b>
  - Cosmos DB, MongoDB, DocumentDB, CouchDB, MarkLogic, OrientDB

<br>

## Column Store

- Stores data using a column oriented model
- Columns in each row are contained within that row
- Each row can have different columns to the other rows
- Extremely quick to load and query
- <b>Use Cases:</b>
  - Sensor Logs [Internet of Things (IOT)], User preferences, Geographic information, Reporting systems, Time Series Data, Logging and other write heavy applications
- <b>Examples:</b>
  - Cosmos DB, Bigtable, Cassandra, Hbase, Vertica, Druid, Accumulo, Hypertable

<br>

## Graph Store

- Focuses on how data relates to other data points
- A node is a specific entity or piece of information
- Edge simplify specifies the relationship between two nodes
