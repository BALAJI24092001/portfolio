---
draft: false
title: "Database Warehousing"
categories: ["Notes"]
---

<!-- tags: ["CS"] -->

I computing, a data warehouse, also known as an enterprise data warehouse, is a system used for reporting and data analysis and is considered a core component of data analysis.

Data warehouses are central repositories of integrated data from one or more different sources. They store current and historical data in one single place.

We use databases for transaction purposes, and the historical data of these transactions and it's previous states are stored in this data warehouses.

Using the process called ETL, the data from the databases are converted and stored in data warehouses. From the data warehouse we get the meta data for analysis, visualization and for additional business intelligence insights.

A data warehouse is a repository (data and metadata) that contains integrated, cleansed, and reconciled data from disparate sources for decision support applications, with an emphasis on online analytical processing.

- **Integrated**: A data warehouse integrates data from multiple data sources. For example, source A and source B may have different ways of identifying a product, but in a data warehouse, there will be only a single way of identifying a product.
- **Time-Variant**: Historical data is kept in a data warehouse. For example, one can retrieve data from 3 months, 6 months, 12 months, or even older data from a data warehouse. This contrasts with a transactions system, where often only the most recent data is kept. For example, a transaction system may hold the most recent address of a customer, where a data warehouse can hold all addresses associated with a customer.
- **Non-volatile**: Once data is in the data warehouse, it will not change. So, historical data in a data warehouse should never be altered.

## Data Warehouse Architecture

![Data Warehouse Architecture](./img/DWHA.png)

## ETL

E: Extract (Extraction of data from different sources) <br>
T: Transform (Clean and convert data into more approprioate structure to store in the warehouse) <br>
L: Load<br>

Three-phase process where data is extracted, transformed and loaded into an output data container. Usually done by application software but can be done manually also.

> Updates in a database are very frequent.

**Extract**: The first stage in the ETL process is to extract data from various sources such as transactional systems, spreadsheets, and flat files. In this step, data from various source systems is extracted which can be in various formats like relational databases, No SQL, XML, and flat files into the staging area. It is important to extract the data from various source systems and store it into the staging area first and not directly into the data warehouse because the extracted data is in various formats and can be corrupted also. Hence loading it directly into the data warehouse may damage it and rollback will be much more difficult. Therefore, this is one of the most important steps of ETL process

**Transform**: In this stage, the extracted data is transformed into a format that is suitable for loading into the data warehouse. In this step, a set of rules or functions are applied on the extracted data to convert it into a single standard format. It may involve following processes/tasks:

- _Filtering_ – loading only certain attributes into the data warehouse.
- _Cleaning_ – filling up the NULL values with some default values, mapping U.S.A, United States, and America into USA, etc.
- _Joining_ – joining multiple attributes into one.
- _Splitting_ – splitting a single attribute into multiple attributes.
- _Sorting_ – sorting tuples on the basis of some attribute (generally key-attribute).

**Load**: After the data is transformed, it is loaded into the data warehouse. This step involves creating the physical data structures and loading the data into the warehouse. In this step, the transformed data is finally loaded into the data warehouse. Sometimes the data is updated by loading into the data warehouse very frequently and sometimes it is done after longer but regular intervals. The rate and period of loading solely depend on the requirements and varies from system to system.

> ETL is used if the whole process is outlet to a different organization, so the data is not directly loaded into the warehouse, rather it is kept in a staging area where is can be scrutinized for saftey issues and then loaded into the warehouse.
> ELT is used if the company itself is handling all the work. Here the data is directly loaded into the warehouse and then transformed and stored in the warehouse.

## Data Warehouse Models

1. Enterprise warehouse:

   - An enterprise warehouse collects all of the information about subjects spanning the entire organization.
   - It provides corporate-wide data integration, usually from one or more operational systems or external information providers, and is cross-functional in scope.
   - It typically contains detailed data aswell as summarized data, and can range in size from a few gigabytes to hundreds of gigabytes, terabytes, or beyond.
   - An enterprise data warehouse may be implemented on traditional mainframes, computer superservers, or parallel architecture platforms. It requires extensive business modeling and may take years to design and build.

2. Data mart:
   - A data mart contains a subset of corporate-wide data that is of value to a specific group of users. The scope is confined to specific selected subjects. For example,a marketing data mart may confine its subjects to customer, item, and sales. The data contained in data marts tend to be summarized.
   - Data marts are usually implemented on low-cost departmental servers that are UNIX/LINUX or Windows-based. The implementation cycle of a data mart is more likely to be measured in weeks rather than months or years. However, it may involve complex integration in the long run if its design and planning were not enterprise-wide.
   - Depending on the source of data, data marts can be categorized as independent or dependent. Independent data marts are sourced from data captured from one or more operational systems or external information providers, or from data generated locally within a particular department or geographic area. Dependent data marts are sourced directly from enterprise data warehouses.
3. Virtual warehouse:

   - A virtual warehouse is a set of views over operational databases. For efficient query processing, only some of the possible summary views may be materialized.
   - A virtual warehouse is easy to build but requires excess capacity on operational database servers.

---

**OLTP (Online Transaction Processing)**

Type of data processing that consists of executing a number of transactions occuring currently. Eg; Online banking, online shopping etc...

**OLAP (Online Analytical Processing)**

Software for performing multi-dimensional analysis at high speeds on large volumes of data from a data warehouse, data mart or some other unified , centralized data store.

| OLTP Systems                                                                                         | OLAP Systems                                                                                               |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Enable the real-time execution of large numbers of database transactions by large numbers of people. | Usually involve querying many records (even all records) in a database for analytical purposes.            |
| Require lightning-fast response times                                                                | Require response times that are orders of magnitude slower than those required by OLTP.                    |
| Modify small amounts of data frequently and usually involve a balance of reads and writes.           | Do not modify data at all; workloads are usually read-intensive.                                           |
| Use indexed data to improve response times                                                           | Store data in columnar format to allow easy access to large numbers of records.                            |
| Require frequent or concurrent database backups                                                      | Require far less frequent database backup.                                                                 |
| Require relatively little storage space                                                              | Typically have significant storage space requirements because they store large amounts of historical data. |
| Usually run simple queries involving just one or a few records                                       | Run complex queries involving large numbers of records.                                                    |

---

## Data Warehouse Schema

1. Star Schema
2. Snowflake Schema
3. Fact Constellation Schema (Galaxy Schema)
