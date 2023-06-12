# MongoDB and Mongoose

## nosql vs sql


### SQL vs NoSQL : High-Level Differences

- SQL databases ae primarily called as Relational Databases whereas NOSQL are primarily called as non-relational or distributed database

- SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores. This means that SQL databases represent data in form of tables which consists of n number of rows of data whereas NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.


- SQL databases have predefined schema whereas NoSQL databases have dynamic schema for unstructured data.


- SQL databases are vertically scalable whereas the NoSQL databases are horizontally scalable. SQL databases are scaled by increasing the horse-power of the hardware. NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load.


- SQL databases uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful. In NoSQL database, queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language). The syntax of using UnQL varies from database to database.


- SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL. NoSQL database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb


- For complex queries: SQL databases are good fit for the complex query intensive environment whereas NoSQL databases are not good fit for complex queries. On a high-level, NoSQL don’t have standard interfaces to perform complex queries, and the queries themselves in NoSQL are not as powerful as SQL query language.


- For the type of data to be stored: SQL databases are not best fit for hierarchical data storage. But, NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.


- For scalability: In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.


- For high transactional based application: SQL databases are best fit for heavy duty transactional type applications, as it is more stable and promises the atomicity as well as integrity of the data. While you can use NoSQL for transactions purpose, it is still not comparable and sable enough in high load and for complex transactional applications.


- For support: Excellent support are available for all SQL database from their vendors. There are also lot of independent consultations who can help you with SQL database for a very large scale deployments. For some NoSQL database you still have to rely on community support, and only limited outside experts are available for you to setup and deploy your large scale NoSQL deployments.


- For properties: SQL databases emphasizes on ACID properties ( Atomicity, Consistency, Isolation and Durability) whereas the NoSQL database follows the Brewers CAP theorem ( Consistency, Availability and Partition tolerance )


- For DB types: On a high-level, we can classify SQL databases as either open-source or close-sourced from commercial vendors. NoSQL databases can be classified on the basis of way of storing data as graph databases, key-value store databases, document store databases, column store database and XML databases.


- Q. What kind of data is a good fit for an SQL database?

- A. Complex queries


- Q. Give a real world example.

- A. An e-commerce store like amazon or stock x 


- Q. What kind of data is a good fit a NoSQL database?

- A. Hierarchical data


- Q. Give a real world example.

- A. Hbase


- Q. Which type of database is best for hierarchical data storage?

- A. NoSQL


- Q. Which type of database is best for scalability?

- A. SQL


- Q. What does SQL stand for?

- A. Structured Query Language


- Q. What is a relational database?

- A. A relational database is a type of database management system (DBMS) that organizes data into tables, which are structured collections of related information.


- Q. What type of structure does a relational database work with?

- A. a tabular structure. It organizes data into tables


- Q. What is a ‘schema’?

- A.  a schema refers to the logical structure or blueprint that defines the organization, relationships, and constraints of a database system. 


- Q. What is a NoSQL database?

- A. a type of database management system (DBMS) that provides a non-relational approach to storing and retrieving data.


- Q. How does it work?

- A. 


- Q. What is inside of a MongoDB database?

- A. the data is organized into collections. A collection in MongoDB is analogous to a table in a relational database. It is a group of related documents that can have different structures and schemas.


- Q. Which is more flexible - SQL or MongoDB? and why.

- A. MongoDB because it provides a higher degree of flexibility in terms of schema, data modeling, and handling complex data structures.


- Q. What is the disadvantage of a NoSQL database?

- A. The disadvantages of NoSQL databases include the lack of standardization, limited support for complex queries and joins, eventual consistency leading to temporary data inconsistencies, increased data redundancy due to replication, potential limitations in tooling and ecosystem support, and a learning curve for developers transitioning from SQL databases. 



