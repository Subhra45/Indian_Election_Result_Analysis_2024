# Indian Lok Sabha Election Result Analysis for 2024
This repository analyses the 2024 Indian Lok Sabha election results using SQL. It provides insights into party and candidate performance, including victory margins, vote shares, and demographic trends. The project features SQL scripts for querying election datasets, aiming to enhance understanding of electoral patterns and voter behaviour in India.

## Key Features of this analysis
Data Querying: Execute complex SQL queries to extract specific insights from large election datasets, allowing for targeted analysis of voting patterns.

Join Operations: Utilize SQL joins to combine data from multiple tables, enabling comprehensive analysis of party performance across different demographics and regions.

Aggregate Functions: Leverage SQL aggregate functions (e.g., SUM, AVG, COUNT) to calculate total votes, average vote shares, and other statistical metrics essential for performance evaluation.

Filtering and Sorting: Apply SQL WHERE clauses and ORDER BY statements to filter results based on criteria such as state, party, or candidate, and sort data for better readability.

Subqueries: Use subqueries to perform nested queries that allow for more complex analysis, such as identifying trends over time or comparing candidate performances.

Data Transformation: Transform raw election data into meaningful insights by using SQL functions for data manipulation, such as CASE statements for categorizing results.

## Schema
```sql
drop table if exists constituencywise_details
create table constituencywise_details
(s_n int,
candidate varchar(300),
party varchar(100),
evm_votes bigint,
postal_votes bigint,
total_votes bigint,
percent_of_votes float,
constituency_id varchar(20));
```

```sql
drop table if exists constituencywise_results
create table constituencywise_results
(s_no int,
parliament_constituency varchar(200),
constituency_name varchar(100),
winning_candidate varchar(200),
total_votes bigint,
margin bigint,
constituency_id varchar(20) primary key,
party_id int);
```

```sql
drop table if exists partywise_results
create table partywise_results
(party varchar(200),
won	int,
party_id int primary key);
```

```sql
drop table if exists states
create table states
(state_id varchar(10) primary key,
state varchar(50));
```

```sql
drop table if exists statewise_results
create table statewise_results
(constituency varchar(50),
constituency_no int,
parliament_constituency varchar(100) primary key,
leading_candidate varchar(200),
trailing_candidate varchar(200),
margin bigint,
status varchar(50),
state_id varchar(10),
state varchar(50));
```
