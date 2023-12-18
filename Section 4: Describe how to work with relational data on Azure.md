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

<br>

## Methods of Provisioning and Deployment

- The Azure portal
  - Convenient but manual
- The Azure command-line interface (CLI)
  - Set of commands to create and manage Azure resources specifically
  - Can run from the operating system command prompt or the CLoud Shell in the Azure portal
  - Suitable if you need to automate service creation
- Azure PowerShell
  - This is a cross-platform task automation and configuration management framework
  - Command-line shell and scripting language that is built on top of .NET
  - Azure provides a series of commandlets (Azure-specific commands) that you can use in PowerShell to create and manage Azure resources.
- Azure Resource Manager templates
  - JSON (JavaScript Object Notation) file template that describes the service, and can be used to create resources

<br>
<br>

# What is Azure SQL Database

Azure SQL Database, a relational database-as-a-service in the cloud with mission critical capabilities.

<br>

## Why SQL Server in Azure?

- Fully managed
- Predictable performance and pricing
- Elastic pool for unpredictable workloads
- 99.99% availability built-in
- Goe-replication services
- Supports existing SQL Server tools, libraries and APIs
- Scalability with no downtime
- Secure and compliant for your sensitive data

<br>
<br>

# Azure IaaS vs Pass Database offering

- SQL Server on Azure VMs
  - SQL Server inside a fully-managed VM in Azure
  - Iaas
  - Migrate without any database change
  - Full control over database engine
  - Can bring existing license

<br>

- Azure SQL Database
  - Database-as-a-service (DBaaS) hosted in Azure
  - PaaS
  - Additional features
  - Pay-as-you-go service
  - Multiple deployment options and tiers

<br>

## Responsibility comparison

- SQL Server on Azure VMs
  - Maintain operating system
  - Maintain SQL Server
  - High Availability
  - Disaster recovery
  - Performance
  - Change control
  - Security

<br>

- Azure SQL Database
  - Security
  - Change control
  - Performance
  - Test the high availability and Disaster recovery
  - Choosing the right service tier

<br>

## Benefits comparison

- SQL Server on Azure VMs
  - Full control over sql server engine
  - Full parity with matching version of on-premises sql server
  - Easy migration from SQL Server on-premises
  - Private IP address within azure VNet
  - 99.99% availability

<br>

- Azure SQL Database
  - Build in advanced intelligence and security
  - Ability to assign necessary resources (CPU/Storage) to individual databases
  - Build-in backups, patching, recovery
  - Most commonly used sql server features are available
  - Online change of resources (CPU/Storage) with no downtime
  - 99.99% availability guaranteed

<br>
<br>

# Azure Database Deployment options

- Azure database Offerings
  - IaaS
    - Deployment option in virtual machine platform
  - PaaS
    - Deployment options such as: Single Database, Elstic Pool Managed Instance
   
<br>

## SQL Server (PaaS) Deployment Options

- Single database
  - Isolated database that is perfect for a application that needs a single data source
  - Each DB with its own guaranteed compute, memory and storage
- Elastic pool
  - Fixed resources will be shared by all databases in the pool
  - Collection of single databases with a shared set of resources such as CPU or memory
- Managed Instance
  - Each managed instance has its guaranteed resources
  - A set of databases that can be used together, easy migration of on-premises databases

<br>

## SQL Server on Virtual Machine

- Full version of SQL Server in the Cloud
- Geographic regions
- Variety of configuration to choose
- Automatic updates
- Automatic backups
- High Availability
- Performance

<br>
<br>

# Azure SQL DB vs. Azure SQL DW

- Azure SQL Database
  - OLTP/CRUD
  - SMP (Symmetric Multi Processing)
  - Vertical Scale
  
<br>

- Azure SQL Data Warehouse
  - OLAP/querting and reporting
  - MPP (Massively Parallel Processing)
  - Horizontal Scale
  - Can pause the virtual server to save cost
  - Polybase

<br>
<br>

# Azure Data Services

### MySQL

- Simple to use open source database management
- Can be used for Linux, Apache, MySQL, and PHP (LAMP) stack apps
- Several editions: Community, Standard, and Enterprise

### Benefits of Azure Database for MySQL

- High availability
- Scalable
- Secure data, both at rest and in motion
- Automatic backups and point-in-time restore for the last 35 days
- Enterprise-level security and compliance with legislation
- Azure Database for MySQL servers provides monitoring functionality to add alerts, and to view metrics and logs

<br>

### MariaDB

- New DBMS, created by the original developers of MySQL
- Compatibility with Oracle Database
- Optimized to improve performance
- Built-in support for temporal data

### Benefits of Azure Database for MariaDB

- Fully managed and controlled by Azure
- Built-in high availability with no additional cost
- Predictable performance, using inclusive pay-as-you-go pricing
- Scaling as needed within seconds
- Secured protection of sensitive data at rest and in motion
- Automatic backups and point-in-time-restore for up to 35 days
- Enterprise-grade security and compliance

<br>

### PostgreSQL

- Hybrid relational-object database
- Enables you to store custom data types, with their own non-relational properties
- Code modules can be added
- Manipulate geometric data, such as lines, circles, and polygons
- pgsql

### Benefits of Azure Database For PostgreSQL

- Provides the same availability, performance, scaling, security, and administrative benefits
- Some features of on-premises PostegreSQL databases are not available in Azure Database for PostgreSQL
- Continue to use pgAdmin tool

<br>

## Migrate data to Azure

- Azure Database Migration Service (DMS)
  - Enables you to restore a backup of your on-premise databases directly to databases running in Azure Data Services
- Replication from an on-premises database

<br>
<br>

# Identify Query Tools

- Azure Portal
- SQL Server Management Studio (SSMS)
- Azure Data Studio
- Sqlcmd Utility
- Visual Studio Code

<br>

## Azure Portal

- Query editor built in to the portal
- Execute queries against your database in Azure SQL Database or data warehouse in Azure Synapse Analytics
- Doesn't support connecting to the master database
- 5-minute timeout for query execution
- No support for IntelliSense for database tables and views
