# What Is a Relational Database?

Introduction

With so many options available, it can be challenging to choose a database solution that perfectly fits your needs. When it comes to [database types](https://phoenixnap.com/kb/database-types), one popular option is a relational database.

**In this article, we will cover the structure of relational databases, how they work, and the advantages and disadvantages of using them. We will also use examples to illustrate how relational databases organize data.**

## Relational Database Definition

A **relational database** is a type of database that focuses on the relation between stored data elements. It allows users to establish links between different sets of data within the database and use these links to manage and reference related data.

Many relational databases use **SQL** (Structured Query Language) to perform queries and maintain data.

### Relational vs Non-Relational Databases

Relational databases focus on relations between data. Hence, relations database need to store data in a highly structured way. This enables faster indexing and query response times and makes the data more secure and consistent.

On the other hand, [NoSQL databases](https://phoenixnap.com/kb/what-is-nosql) don't need to rely on structure as much, which allows them to store large amounts of data, remain flexible, and easily scale storage and performance.

**Note:** For a more in-depth look at the differences between relational and non-relational databases, check out our [article comparing SQL and NoSQL](https://phoenixnap.com/kb/sql-vs-nosql).

## How Is Data in a Relational Database System Organized?

Relational database systems use a model that organizes data into **tables** of **rows** (also called ***records*** or ***tuples\***) and **columns** (also called ***attributes\*** or ***fields\***). Generally, columns represent categories of data, while rows represent individual instances.

Let's use a digital storefront as an example. Our database might have a table containing customer information, with columns representing customer names or addresses, while each row contains data for one individual customer.

![Example of a table in a relational database](https://phoenixnap.com/kb/wp-content/uploads/2021/06/relational-database-table-elements.png)

These tables can be linked or related using **keys**. Each row in a table is identified using a unique key, called a **primary key.** This primary key can be added to another table, becoming a **foreign key.** The primary/foreign key relationship forms the basis of the way relational databases work.

Returning to our example, if we have a table representing product orders, one of the columns might contain customer information. Here, we can import a primary key that links to a row with the information for a specific customer.

![Forming a relation between two tables](https://phoenixnap.com/kb/wp-content/uploads/2021/06/relational-database-table-relation-example.png)

This way, we can reference the data or duplicate data from the customer information table. It also means that these two tables are now related.

**Note:** If you are new to databases, our post [What Is A Database](https://phoenixnap.com/kb/what-is-a-database) is a good starting point to learn everything you need to know.

## Relational Database Examples

Now that we've covered how they work, here are some of the most popular examples of relational databases:

### MySQL

![MySQL, a popular relational database.](https://phoenixnap.com/kb/wp-content/uploads/2021/06/relational-database-mysql-logo.png)

MySQL was developed as an open-source management system for relational databases until it was acquired by Sun Microsystems (now Oracle Corporation). It is still available under an open-source license, with the addition of different proprietary licenses.

MySQL features built-in replication support with [ACID](https://phoenixnap.com/kb/acid-vs-base) compliance, [shared-nothing clustering](https://phoenixnap.com/kb/shared-nothing-architecture), and supports multiple storage engines. However, using some storage engines can cause SQL not to work properly.

MySQL excels at fast data input and scalability while maintaining [high availability](https://phoenixnap.com/infrastructure-solutions/high-availability-solutions) and performance. This makes it extremely useful for web and application development.

**Note:** If you are interested in trying out MySQL, check out our [guide to installing MySQL on Ubuntu](https://phoenixnap.com/kb/install-mysql-ubuntu-20-04). We also have a helpful [overview of MYSQL data types](https://phoenixnap.com/kb/mysql-data-types).

### PostgreSQL

![PostgreSQL, a relational database.](https://phoenixnap.com/kb/wp-content/uploads/2021/06/relational-dtabase-postgresql-logo.png)

PostgreSQL is a free relational database manager available under an open-source license. It shares some features with MySQL, with the notable addition of MVCC (multi-version concurrency control), making it ACID compliant.

PostgreSQL retains a high level of performance and flexibility, even when handling large databases. It's the right choice for users that need high read/write speeds and extensive data analysis.

Some notable users of PostgreSQL include Reddit, Skype, and Instagram.

**Note:** Also, have a look at our [guide to installing PostgreSQL on Ubuntu](https://phoenixnap.com/kb/how-to-install-postgresql-on-ubuntu) and learn [how to create your first database](https://phoenixnap.com/kb/postgres-create-database). And if you want to find out more about different built-in data types available in PostgreSQL, read our article [PostgreSQL data types](https://phoenixnap.com/kb/postgresql-data-types).

### MariaDB

![MariaDB, a MySQL fork.](https://phoenixnap.com/kb/wp-content/uploads/2021/06/relational-database-mariadb-logo.png)

MariaDB started as a community-driven fork of MySQL after the latter was purchased by Oracle. It is still open-source, available under the [GNU General Public License](https://phoenixnap.com/glossary/gnu-general-public-license).

MariaDB builds upon the MySQL base by adding support for even more storage engines and fixing storage engine limitations. This allows it to perform even faster than MySQL and run both SQL and NoSQL in a single database.

Notable MariaDB users include Google, Mozilla, and the Wikimedia Foundation.

**Note:** Check out our [guide to installing MariaDB on Ubuntu](https://phoenixnap.com/kb/how-to-install-mariadb-ubuntu) and [how to install it on CentOS](https://phoenixnap.com/kb/how-to-install-mariadb-on-centos-7).

### SQLite

![SQLite](https://phoenixnap.com/kb/wp-content/uploads/2021/06/relational-database-sqlite-logo.png)

Unlike other entries on this list, SQLite is not a client-server database manager but rather embedded into the end application. This makes it lightweight and able to work with a wide array of systems and platforms.

It also causes some limitations, as SQLite only partially provides triggers, has a limited **`ALTER TABLE`** function, and cannot write to views. It also limits the maximum size of the database to 32,000 columns and 140 TB.

SQLite is, therefore, best used as a database component for other applications. Notable uses include popular browsers, such as Google Chrome, Mozilla Firefox, Opera, and Safari.

## What Is Relational Database Management System?

A **database management system** (DBMS) is a software solution that helps users view, query, and manage databases.

[Relational database management systems (RDBMS)](https://phoenixnap.com/glossary/relational-database-management-system-rdbms/) are a more advanced subset of DBMS, handling relational databases.

### DBMS vs RDBMS

Here are some of the differences between more general DBMS solutions and RDBMS:

| **DBMS**                                                    | **RDBMS**                                                    |
| ----------------------------------------------------------- | ------------------------------------------------------------ |
| Stores smaller amounts of data as files, with no relations. | Stores large amounts of data as tables that are related to each other. |
| Can only access one data element at a time.                 | Can access multiple data elements at the same time.          |
| Working with large amounts of data makes fetching slower.   | Relational approach allows data fetching to remain fast even for large databases. |
| No database normalization.                                  | Allows [database normalization](https://phoenixnap.com/kb/database-normalization). |
| Does not support distributed databases.                     | Supports [distributed databases](https://phoenixnap.com/kb/distributed-database). |
| Supports a single user.                                     | Supports multiple users.                                     |
| Lower security level.                                       | Multiple security levels.                                    |
| Low software and hardware requirements.                     | High software and hardware requirements.                     |

## Relational Database Advantages and Disadvantages

Like any other database model, there are advantages and disadvantages to using relational databases:

### Advantages

Since relational databases use tables of rows and columns, they display data more simply than some other database types, making them easier to use.

This tabular structure shifts the focus to handling data, which allows faster performance and the use of complex, high-level queries.

Finally, relational databases make it easy to scale data by simply adding rows, columns, or entire tables without changing the overall database structure.

### Disadvantages

There are limits to how well relational databases can scale. In terms of sheer size, some databases have fixed limits on column lengths. If your database is built on a single [dedicated server](https://phoenixnap.com/servers/dedicated), scaling requires buying more server space, proving expensive in the long run.

Also, constantly adding new elements to a database can make it so complex it becomes difficult to form relations between new pieces of data. Complicated data relations also slow down querying and negatively affect performance.

Conclusion

After reading this article, you should have a solid understanding of how relational databases work. You should also be familiar with some of the most notable examples of relational database management systems.