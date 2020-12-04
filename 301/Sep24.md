# DB Normalization

## Database Normalization Explained in Simple English

> Database normalization
  A process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included.
Three main reasons to normalize a database
To Minimize duplicate data
Duplicated information present two problems
It increases storage and decrease performance
It becomes more difficult to maintain data changes
To minimize or avoid data modification issues
Three modification anomalies that occur:
Insert anomaly
Facts we cannot record until we know information for the entire row.
Update anomaly
If we have the same information in several rows, then inconsistencies appear.
Deletion anomaly
Causes loss of information and set of facts
To simplify queries
You can eliminate or reduce these anomalies by separating the data into different tables. This puts the data into tables serving a single purpose.
Three common forms of database normalization: 
> 1st normal form (1NF)
    The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
> 2nd normal form (2NF)
    The table is in first normal form and all the columns depend on the table’s primary key.
> 3rd normal form (3NF)
    The table is in second normal form and all of its columns are not transitively dependent on the primary key