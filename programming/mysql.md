# MySql



### **ACID**

 \(Atomicity, Consistency, Isolation, Durability\): The rules that guarantee the database will be consistent when the transaction get finished. In other words it commits all the changes only if all the queries will run without any failure and it guarantee that before and after a transaction the state of database is valid. It locks the database to avoid conflicts and after the transaction finished successfully it will write the data on the disk

1. Atomicity: Either all the steps should be applied to the database, or none of them should.  Guarantee each transaction is treated as a single statement although the transactions usually composed as multiple statement. Atomicity guarantee that in every stage, if any failure happened database will remain unchanged.
2. Consistency: The consistency feature states that every transaction should leave the database in a valid state.  ensures that a transaction can only bring the database from one valid state to another. Any data written to the database must follow the valid rules
3. Isolation: It locks data while a transaction is being committed to the database  Determines how and when changes made by one transaction become visible to the other .
4. Durability: Once a transaction is complete, it is guaranteed that all of the changes stored in a hard drive.

### Engines: 

1. InnoDB: New, support transactions, support relations, foreign key, row level locking
2. MyISAM
3. HEAP: in memory table

### EXPLAIN: 

provide information about a query

### Optimize query:

Add index to the field used in where, order by and group by  
Avoid using the leading wild card

### What is indexes?

* A database index allows a query to efficiently retrieve data from a database. 
* One or more indexes in table
* Need more space on hard to write the indexes
* if you write into a table \(`UPDATE` or `INSERT`\) with one index, you have actually two writing operations in the file system



