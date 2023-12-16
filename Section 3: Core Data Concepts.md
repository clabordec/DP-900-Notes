# Data Types

Data is a collection of facts such as numbers, descriptions and observations used in decison making

<br>

## Data Classificatoin

- Structured Data
- Semi-Structured Data
- Unstructured Data

<br>

### Structured Data

Structured data us typically tabular data that is repersented by rows and columns in a database. <br>
Example - Datawarehouse, ERP, CRM

<br>

### Semi-Structured Data

- It has some organiztional framework but does not have the complete structure that is required to fit in a relation database. <br>
Example - CSV, XML, JSON


<br>

### Unstructured Data

Unstructured data is data which is not organized in any predefined manner. <br>
Example - audio and video files, and binary data files

<br>

## Data Storage in Cloud

- Structured Data - Azure SQL Database
- Semi-Structured Data - AZure Cosmos DB
- Unstructured Data - Azure Blob Storage

<br>
<br>

# Data File Formats

## How to choose file formats?

- Type of data (structured, semi-structured, unstructured)
- How applications will read or write
  - If you have a OLTP system or transactional system, then you'll be dealing with a lot of writing statements.
  - If you have an OLAP system or analystical system such as a data warehouse, you'll read data more efficiently. 
- How data is going to be used - Storage vs processing?

<br>

## Delimited text files

- Data is stored in plain text format with specific field delimeters and row terminators
- Common formats
 - Comma-separated values (CSV)
 - Tab-separated values (TSV)
- Advantages:
 - Easy to read and parse
- Disadvantages
 - Difficult to parse if data itself has commas
 - Data type is not forced consistent

<br>

## Extensible Markup Language (XML)

- Used tags enclosed in brackets `(<../>)` to define elements and attributes
- Created to store and transport data without being dependent on software or hardware tools

<br>

## Javascript Object Notation (JSON)

- Stored with the .json extension
- Supported by most programming languages
- Widely accepted format on the web
 - Can be shard across the network
- Easy - human-readable text
- Requires less formatting and is good alternative for XML
- Disadvantages:
  - No schema enforcing
  - Quite a big size because of repeated keys

<br>

## Binary Large Object (BLOB)

- Stored as binary data (1's and 0's)
- Collection of binary data stored as a single entity
- Blobs are typically images, audio or other multimedia objects, though sometimes binary executable code is stored as a blob
- They can exist as persistent values inside some databases, or exit at runtime as program variables in some languages

<br>

## Optimized file formats

- CSV, JSON, XML, BLOB
  - Advantage - Human-readable
  - Disadvantage - Not optimized for storage space or processing
- Optimized file formats
  - Enable compression, indexing, and efficient storage and processing
  - Avro, ORC, Parquet

<br>

### Avro

- Created by Apache
- Row-based format
- Compact, fast, binary data format
- Header describe the structure of data in the record
- Header is stored in JSON
- Application uses the information in the header to parse the bibary data and extract the fields it contains
- Good format for compressing data and minimizing storage and network bandwidth requirements
- Can't read data without using avro tools like JSON

<br>

### ORC

- ORC - Optimized Row COlumn format
- Organizes data into columns rather than rows
- ORC only supports Hadoop HIVE and PIG
- File structure
  - File footer stores auxiliary information
    - List of stripes in the file
    - Number of rows per stripe
    - Each column's data type
    - Column-level aggregates count, min, max and sum
  - Strip footer contains a directory of stream locations
  - Row data is used in table scans
  - Index data includes min and max values of each column and the row positions within each column

<br>

### Parquet

- Columnar data format
- Contains row groups
  - Data for each column is stored together in the same row group
- Includes metadata that describes the set of rows found in each chunk
- Specializes in storing and processing nested data types efficiently
- Supports very efficient compression and encoding schemes
- Available to any project in the Hadoop ecosystem (Hive, Hbase, MapReduce, Pig, Spark)
- Exceptionally good for read-intensive jobs

<br>

### Avro vs Parquet vs ORC

- How to choose file format?
  - Large files (TB, PB) - Avro
  - ETL Jobs - Avro
  - Ease of maintenance - Parquet
  - Hive - ORC
  - Spark - Parquet

<br>
<br>

# OLTP vs OLAP

## OLTP

- Many small transactions
- Current data
- Used to run the business
- Highly detailed
- Typically in the GB scale
- Processing performance limit

<br>

## OLAP

- Low volume but complex queries
- Historic, non-volatile data
- Used to analyze the business
- Consolidated and summarized
- TB and above scale
- No limit, pause/resume compute
