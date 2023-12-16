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
