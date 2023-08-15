# NoSQL Database Types

## Introduction

NoSQL is an alternative to traditional SQL databases. Over time, relational databases proved to be inadequate for specific use cases. These limitations varied depending on the application they needed to support.

Different developers focused on overcoming different challenges according to their needs. As a result, you now have different types of NoSQL databases.

**This tutorial focuses on NoSQL database types.** For a more in-depth guide about NoSQL, its features, and when to use it, visit our article [What Is NoSQL?](https://phoenixnap.com/kb/what-is-nosql)

## Types of NoSQL Databases

There are four popular NoSQL database types:

1. Key-Value Databases
2. [Document Databases](https://phoenixnap.com/kb/document-database)
3. Wide-Column Databases
4. [Graph Databases](https://phoenixnap.com/kb/graph-database)

**Note:** Familiarize yourself with core concepts about databases by reading our post [What Is A Database?](https://phoenixnap.com/kb/what-is-a-database)

### Key-Value Database

Key-value databases are the simplest type of NoSQL database. Thanks to their simplicity, they are also the most scalable, allowing [horizontal scaling of large amounts of data](https://phoenixnap.com/glossary/horizontal-scaling).

These NoSQL databases have a dictionary data structure that consists of a set of objects that represent fields of data. Each object is assigned a unique key. To retrieve data stored in a particular object, you need to use a specific key. In turn, you get the value (i.e. data) assigned to the key. This value can be a number, a string, or even another set of key-value pairs.

![Key-Value database.](https://phoenixnap.com/kb/wp-content/uploads/2021/04/key-value-database.png)

Unlike traditional relational databases, key-value databases do not require a predefined structure. They offer more flexibility when storing data and have faster performance. Without having to rely on placeholders, key-value databases are a lighter solution as they require fewer resources.

Such functionalities are suitable for large databases that deal with simple data. Therefore, they are commonly used for **caching**, **storing**, and **managing user sessions**, **ad servicing**, and **recommendations**.

[Redis](https://phoenixnap.com/kb/install-redis-on-ubuntu-20-04), Project Voldemort, and Riak are just some examples of key-value databases.

**Note:** Redis is one of the most popular key-value [NoSQL databases](https://phoenixnap.com/kb/nosql-database-list). It features great flexibility and supports a wide variety of [data types](https://phoenixnap.com/kb/redis-data-types-with-commands).

### Document Database

A document database is a type of NoSQL database that consists of sets of key-value pairs stored into a document. These documents are basic units of data which you can also group into [collections (databases)](https://phoenixnap.com/kb/create-database-mongodb) based on their functionality.

![Document database.](https://phoenixnap.com/kb/wp-content/uploads/2021/04/document-database.png)

Being a NoSQL database, you can easily store data without implementing a schema. You can transfer the object model directly into a document using several different formats. The most commonly used are JSON, BSON, and XML.

Here is an example of a simple document in JSON format that consists of three key-value pairs:

```
{ "ID" : "001", "Name" : "John", "Grade" : "Senior", }
```

What’s more, you can also use nested queries in such formats, providing easier data distribution across multiple disks and enhanced performance.

For instance, we can add a nested value string to the document above:

```
{ "ID" : "001", "Name" : "John", "Grade" : "Senior", "Classes" : {      "Class1" : "English"      "Class2" : "Geometry"       "Class3" : "History"   }  }
```

Due to their structure, document databases are optimal for use cases that require flexibility and fast, continual development. For example, you can use them for **managing user profiles**, which differ according to the information provided. Its schema-less structure allows you to have different attributes and values.

Examples of NoSQL document databases include [MongoDB](https://phoenixnap.com/kb/how-to-install-mongodb-ubuntu), CouchDB, [Elasticsearch](https://phoenixnap.com/kb/?s=elasticsearch), and others.

### Wide-Column Database

Wide-column stores are another type of NoSQL database. In them, data is stored and grouped into separately stored columns instead of rows. Such databases organize information into columns that function similarly to tables in relational databases.

![Row-oriented vs column-oriented databases.](https://phoenixnap.com/kb/wp-content/uploads/2021/04/column-oriented-database.png)

However, unlike traditional databases, wide-column databases are highly flexible. They have no predefined keys nor column names. Their schema-free characteristic allows variation of column names even within the same table, as well as adding columns in real-time.

The most significant benefit of having column-oriented databases is that you can store large amounts of data within a single column. This feature allows you to reduce disk resources and the time it takes to retrieve information from it. They are also excellent in situations when you have to spread data across multiple servers.

Examples of popular wide-column databases include Apache Cassandra, HBase, and CosmoDB.

**Note:** If you want to see a side-by-side comparison of a document database and a wide-column database, take a look at [Cassandra Vs MongoDB – What Are The Differences](https://phoenixnap.com/kb/cassandra-vs-mongodb).

### Graph Database

Graph databases use flexible graphical representation to manage data.

These graphs consist of two elements:

1. **Nodes** **(for storing data entities)**
2. **Edges** **(for storing the relationship between entities)**

These relationships between entities allow data in the store to be linked together directly and, in many cases, retrieved with one operation. Nodes and edges have defined properties, and by using these properties, you can query data easily.

![Graph database example.](https://phoenixnap.com/kb/wp-content/uploads/2021/04/graph-database-example.png)

Since this type of data-storing is quite specific, it is not a commonly used NoSQL database. However, there are certain use cases in which having graphical representations is the best solution. For instance, social networks often use graphs to store information about how their users are linked.

OrientDB, RedisGraph, and Neo4j are just some examples of graph databases you should consider using.

Conclusion

After reading this article, you should understand the basics of the four prominent NoSQL database types.

Although they all have different use cases, they all share the main benefits of NoSQL databases.