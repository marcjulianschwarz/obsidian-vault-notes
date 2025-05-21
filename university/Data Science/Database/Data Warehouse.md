---
uni-module: "KDD"

alias: ["DW", "DWH"]
---

# Data Warehouse

A datawarehouse is **subject-oriented** which means that it provides simple and concise views for particular subjects by for example excluding non-relevant data.
It tries to **integrate** multiple heterogeneous data sources into one consistent "database" by doing [[Extract Transform Load]], [[Data Cleaning]] and [[Data Integration]] over a **long time horizon** of data (usually 5-10 years).
It is **nonvolatile** and thus data needs to be copied to the datawarehouse which only has the three **operations** of the initital loading, over night refreshes and access of data.

> [!NOTE] Definition
> Subject-oriented, integrated, time-variant and nonvolatile collection of data in support of decision-making process.

![[Bildschirmfoto 2022-05-23 um 11.36.58.png]]
based on [[Multidimensionale Datenmodellierung]]

## Usage

- Information Processing
  - Querying
  - statistical analysis
  - reporting
- Analytical Processing
  - Multidimensional analyis
  - [[OLAP]] operations
- Data Mining
  - KDD

## Why

Regular [[DBMS]] are tuned for [[OLTP]] which doesn't have the neccesary operations and functions which are being used for data mining.

- [[DBMS]], tuned for OLTP, access methoStds, indexing, concurrency, recovery
- Data Warehouse, tuned for OLAP, complex queries, mdm view, consolidation
- historical data, consolidation

## Models

- [[Enterprise Warehouse]]
- [[Data Mart]]
- [[Virtual Warehouse]]

## Modeling

A data warehouse can be modeled with different [[Internes Schema|schemas]] in mind:

- [[Star Schema]]
- [[Snowflake Schema]]
- [[Fact Constellation]]

## Aggregation

[[Aggregationstypen auf MDMs|Aggregation Type]]
