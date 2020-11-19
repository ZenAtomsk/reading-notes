# **DB Normalization**

[Database Normalization EssentialSQL.com](https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/)

There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively.

1. [First Normal Form](https://www.essentialsql.com/get-ready-to-learn-sql-8-database-first-normal-form-explained-in-simple-english/) – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.

2. [Second Normal Form](https://www.essentialsql.com/get-ready-to-learn-sql-10-database-second-normal-form-explained-in-simple-english/) – The table is in first normal form and all the columns depend on the table’s primary key.

3. [Third Normal Form](https://www.essentialsql.com/get-ready-to-learn-sql-11-database-third-normal-form-explained-in-simple-english/) – the table is in second normal form and all of its columns are not transitively dependent on the primary key

## **Introduction to Database Normalization**

process used to organize a database into tables and columns.

a table should be about a specific topic and only supporting topics included

There are three normal forms most databases adhere to using. As tables satisfy each successive database normalization form, they become less prone to database modification anomalies and more focused toward a sole purpose or topic.

## **Reasons for Database Normalization**

There are three main reasons to normalize a database.

1. to minimize duplicate data
2. to minimize or avoid data modification issues
3. to simplify queries

## **Data Duplication**

Duplicated information presents two problems:
1. increases storage and decrease performance.
2.  becomes more difficult to maintain data changes.

## **Modification Anomalies**

There are three modification anomalies that can occur:
1. Insert Anomaly
  - There are facts we cannot record until we know information for the entire row.
2. Update Anomaly
  - If we don’t update all rows, then inconsistencies appear.
3. Deletion Anomaly
  - Deletion of a row causes removal of more than one set of facts. deleting that row cause us to lose information about other topics

## **Search and Sort Issues**

easier to search and sort your data.

