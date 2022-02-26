# Data Modeling

## Review, Research, and Discussion

1. Name 3 advantages to Test Driven Development? 
*  Refactoring is easier because each feature has been thoroughly tested.
* High test coverage ,Each feature has its own test.
* Tests describe the code — Test code demonstrates how the code should be utilized.

2. In what case would you need to use `beforeEach()` or `afterEach()` in a test suite?

* `beforeEach()`: *for tests that use a certain global state for each test, such as resetting test data in a database before each run*
* `afterEach()`: *If a promise is returned by the function, Jest waits for it to resolve before proceeding.*

3. What is one downside of Test Driven Development.
* It may be tough to write the tests, especially if they go beyond unit testing.

4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes? 
* ES6 Classes: This can be thought of as a syntax base for constructor functions and objects created with the new operator.
* Constructor/Prototype Classes: This too makes use of a new operator for object generation, but it concentrates on how the objects are created.

5. Why REST?
* They provide you a lot of flexibility. REST can accommodate many sorts of calls, return diverse data formats, and even change fundamentally with the correct implementation of hypermedia because data is not linked to resources or functions.

## Important Vocabulary

- **functional programming:** *Functional programming entails making the greatest use of functions in order to create clean and maintainable software.*

- **Object-oriented programming (OOP)** *Object-oriented programming (OOP) is a computer programming approach that organizes software design around data, rather than functions and logic. An object is a data field that has distinct features and behavior.*

- **class** *Classes serve as a starting point for the creation of things. They wrap data with code that allows them to work with it.*

- **super** *is used to invoke the corresponding methods of the super class.*

- **this** *This keyword denotes an object. Which object is utilized depends on how this is invoked (used or called).*

## nosql vs sql

### nosql
*NoSQL (not only SQL) databases are non-tabular databases that store data differently than relational tables. NoSQL databases are classified into several categories based on their data model. Document, key-value, wide-column, and graph are the most common. They offer flexible schemas and can quickly scale with big amounts of data and significant user demands.*

### NoSQL Database Examples
1- MongoDB

*Mongodb is a popular document-based NoSQL database since it stores data in JSON-like documents. It is a non-relational database with an evolving schema. It was created by the founders of DoubleClick and is written in C++.*

**MongoDB benefits and strengths:**

-  Speed: It performs well for simple searches since all linked data is contained in a single document, eliminating the need for join procedures.

- Scalability: It is horizontally scalable, which means that instead of relying on a stand-alone resource, you may minimize workload by increasing the number of servers in your resource pool.

- Easy to manage: It is simple to use for both developers and administrators. This also allows for database sharding.

-  Dynamic Schema: It allows you to alter your data schema without changing the existing data.

2- CouchDB

*CouchDB is a NoSQL database that is based on documents. It keeps data in the form of JSON documents.*

**CouchDB benefits and strengths:**

- Schema-less: As a part of the NoSQL family, it also has dynamic schema, which makes it more flexible, and it stores data in the form of JSON documents.

- HTTP query: You can view your database documents through your web browser.

- Conflict Resolution: It offers automatic conflict identification, which is useful in a distributed database.

- Simple Replication: Replication is simple to set up.

3- Redis

*is Open Source NoSQL database that is popular due to its lightning-fast performance. It is written in the ANSI C programming language.*

**Redis benefits and strengths:**

- Data structures: Redis delivers so efficient data structures that it is sometimes referred to as a data structure server. Database keys can be hashes, lists, texts, sorted or unsorted collections.

- Redis as a Cache: To boost performance, you can utilize Redis as a cache by implementing keys with a restricted period to live.

- Very fast: Because it works with in-memory datasets, it is considered one of the quickest NoSQL servers.

### SQL Database

*SQL databases are commonly referred to as Relational Database Management Systems (RDBMS), whereas NoSQL databases are commonly referred to as non-relational or distributed databases.*

### SQL Database Examples

1- MySQL Community Edition

*MySQL is a well-known open-source database. It is typically stacked with Apache and PHP, but it may also be stacked with nginx and server-side javascripting using Node js.*

**MySQL benefits and strengths:**

- Replication: By replicating the MySQL database across numerous nodes, the work burden is significantly decreased, boosting the scalability and availability of the business application.

- Sharding: MySQL sharding is important when a high traffic website has a significant number of write operations. The program is partitioned across numerous servers by sharding MySQL servers, breaking the database into small bits. This is cost effective since low-cost servers can be installed for this purpose. 

- Memcached as a NoSQL API to MySQL: Memcached can be used to improve the efficiency of data retrieval operations, offering the server a NoSQL API.

- Maturity: This database has been around for a long time, and a lot of community input and testing has gone into it, resulting in a very reliable database.

- Extensive Platform and Language Support: MySql is available for all major systems, including Linux, Windows, Mac, BSD, and Solaris. It also has Node.js, Ruby, C#, C++, C, Java, Perl, PHP, and Python connectors.

- Cost - effective: It is open source and free.

2- MS-SQL Server Express Edition

*It is a robust and user-friendly database with Microsoft compatibility that has good stability, reliability, and scalability.*

**MS-SQL benefits and strengths:**

- Integrated Development Environment (IDE): Microsoft Visual Studio, SQL Server Management Studio, and Visual Developer tools make development easier and boost developer productivity.

- Disaster Recovery: It provides an effective disaster recovery mechanism, which includes database mirroring, fail over clustering, and RAID partitioning.

- Cloud backup: When you perform a cloud backup of your database, Microsoft also provides cloud storage.

3- Oracle Express Edition 

*It is a restricted edition of the Oracle Enterprise Edition server with some restrictions. This database is available for free development and deployment.*

**Oracle benefits and strengths:**

- Easyto Update: It is simple to upgrade to a newer version or to an enterprise edition.

- Wide platform support: It works on a variety of platforms, including Linux and Windows.

- Scalability: Although the scalability of this database is not as cost effective as that of the MySQL server, the solution is very dependable, secure, readily manageable, and productive.

## sql modeling techniques 

### The major elements at model relational database table are : 

1. The Table Name, which appears at the top of the table.

2. The Primary Keys. Each row in a table is uniquely identified by its primary key. A table usually contains one primary key, although it can have more. When a key has more than one column, it is referred to as a compound key.

3. Table Columns - A table can have one or more columns. To keep the diagrams as basic as possible.

4. Foreign Key - A column or combination of columns that corresponds to a primary key in another table.

## sequelize api 

*Sequelize is a Node.js ORM tool that supports Postgres, MySQL, MariaDB, SQLite, Microsoft SQL Server, Amazon Redshift, Snowflake's Data Cloud, DB2, and IBM i. It has strong transaction support, relations, eager and lazy loading, read replication, and other features.*

#### reference: 

- [nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)
- [sql modeling techniques](https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/)
- [sequelize api ](https://sequelize.org/master/manual/getting-started.html)

[back to main page](https://hala277.github.io/advanced-js-reading-notes)