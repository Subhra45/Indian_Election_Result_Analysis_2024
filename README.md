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
create table if not exists constituencywise_details
(s_n int,
candidate varchar(300),
party varchar(100),
evm_votes bigint,
postal_votes bigint,
total_votes bigint,
percent_of_votes float,
constituency_id varchar(20));
```
