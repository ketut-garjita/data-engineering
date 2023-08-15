# **Database Relationship Types & How They Are Established**

Introduction

The main feature of [relational databases](https://phoenixnap.com/kb/what-is-a-relational-database) is relationships. Different relationship types control how the data and tables relate to one another. Establishing links between tables through relationships makes this [database type](https://phoenixnap.com/kb/database-types) unique, and knowing how relationships work helps broaden database modeling capabilities.

**This article explains different relationship types and how they look through practical examples.**

## How Are Relationships Established?

The two following elements define how a database relationship is established:

- **Primary key** - A column whose value uniquely identifies a table record.
- **Foreign key** - A column whose values reference the primary key of another table.

A connection between a parent table and the child table exists by referencing the parent's primary key. The reference's behavior defines the relationship type between two database tables.

[A database](https://phoenixnap.com/kb/what-is-a-database) utilizes relationships between two tables through [JOIN ](https://phoenixnap.com/kb/mysql-join)[statements](https://phoenixnap.com/kb/mysql-join) in a structured query language (SQL).

## Why Are Relationships Important In a Database?

Relationships in a database help create meaningful information. As a result, database relationships result in:

- **Reduced data redundancy**. Relationships help reference information stored in existing tables, reducing repetition.
- **Better organized databases**. Relationships help implement [database normalization](https://phoenixnap.com/kb/database-normalization) techniques. Normalization helps yield a better organized and robust database.
- **Referential integrity**. As databases grow, joins, queries and sorting become expensive. Relationships help reduce the number of transactions and improve data validity.

Established database relationships ensure an [RDBMS](https://phoenixnap.com/glossary/relational-database-management-system-rdbms) is viable, flexible, and stable.

## Database Relationship Types

A relational database implements three different types of relationships:

1. **One-to-one** (1:1)
2. **One-to-many** (1:N)
3. **Many-to-many** (N:N)

A line connecting two tables represents a relationship, while the symbols on the line's end represent the exact relationship type.

For example, in ER diagrams, "one" and "many" relationship cardinalities appear as the following symbols:

- A perpendicular line (**one**).
- Crow's feet (**many**).
- A circle (**zero**).

The symbols combine to form complex relationship types.

![er diagram relationship cardinality](https://phoenixnap.com/kb/wp-content/uploads/2022/07/er-diagram-relationship-cardinality.png)

**Note:** The first two options are ambiguous and should only be used when business rules are not specifically defined.

Below are detailed explanations for each relationship type with examples.

### One-to-One Relationship in a Database

A one-to-one relationship (1:1) in a database has **one record on each side** of the relationship. Every primary key relates to at most one entry from another table, making the foreign key unique.

One-to-one relationships appear from enforced business rules and are not typical. Combining two tables with a one-to-one relationship does not break normalization rules.

**One-to-One Relationship Example**

A simple example to demonstrate a one-to-one relationship is with capital cities. One country (or state) has only one capital city, and one capital city belongs to only one country (or state).

Two tables with information about countries and capital cities connect in a database using a **primary key**. For example, when added to the country table, the unique ID of a capital city (its primary key) becomes a **foreign key**, creating a relationship.

![One to one relationship](https://phoenixnap.com/kb/wp-content/uploads/2022/07/one-to-one-relationship.png)

In this case, the one-to-one relationship is mandatory. Every country *must* have a unique capital city, and the foreign key should be unique to ensure the connection is 1:1.

**Note:** Other ways to create a 1:1 relationship would be to use the **`country_id`** as a unique identifier for the capital table, or reference the **`country_id`** as a unique foreign key.

### One-to-Many Relationship in a Database

A one-to-many (1:N) relationship in a database has a **single entry on one side and multiple entries on the other end**. Every primary key corresponds to one or more records from another table. In this case, the foreign key is not unique.

One-to-many relationships are natural and often appear as a logical connection in database modeling.

**One-to-Many Relationship Example**

An example of a one-to-many relationship is the connection between a mother and children. A mother can have many kids, but every child belongs to one mother only.

A database containing two tables with information about mothers and children connects using a **primary key**. When added to the child table, the unique ID from a mother becomes a **foreign key**. Different children can have the same mother.

![One to many relationship](https://phoenixnap.com/kb/wp-content/uploads/2022/07/one-to-many-relationship.png)

The relationship is mandatory on both ends, and at least one entry must exist in both tables to establish a connection.

### Many-to-Many Relationship in a Database

Many-to-many (N:N) relationships in a database have **multiple entries on both ends** of the relationship. Since numerous entries may exist on both ends, a standard solution is to create an **association** (junction, join) table with foreign keys from both tables.

Many-to-many relationships are a common practice with relational databases implemented in web technologies, such as [ecommerce](https://phoenixnap.com/ecommerce-hosting) websites.

**Many-to-Many Relationship Example**

A many-to-many relationship exists between books and authors. For example, a single book can have multiple authors. Likewise, a single author can have numerous books.

If there is a table containing books and another with authors, the best way to establish the relationship between the two is through a **new table**. The new table has foreign keys from both parent tables, creating a many-to-many relationship.

![Many to many relationship](https://phoenixnap.com/kb/wp-content/uploads/2022/07/many-to-many-relationship.png)

Performing different types of JOIN queries fetches data from both tables efficiently while protecting the original tables from redundancies.

Conclusion

After reading this article, you know about the different relationship types and how they help provide a practical modeling solution in relational databases.