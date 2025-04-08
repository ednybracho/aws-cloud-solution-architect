# Databases on AWS

Databases are purpose-built on AWS, which means that each AWS database service is built for a specific use case or set of use cases. Using a database that is a best fit for the use case can save a lot of time in development hours. In the past, it was common to use relational databases for everything because they were the most commonly operated database on premises. With AWS, you can run different types of databases more easily without managing the infrastructure yourself. This can lead to making decisions that are more aligned with the use case and aren’t limited to in-house skill for database administration.

For this weeks customer, Morgan chose Amazon DynamoDB as the database choice because the customer is using it as a simple lookup table, there is no need for complex SQL queries or joins across tables, and the serverless nature of the table makes it easy to operate over time.

For a high-level overview of the AWS database services, see [AWS Cloud Databases.](https://aws.amazon.com/products/databases/)

## Amazon Aurora

Amazon Aurora is a fully managed relational database engine that's compatible with MySQL and PostgreSQL. You can use the code, tools, and applications for your existing MySQL and PostgreSQL databases with Aurora.

Aurora wasn’t chosen for this architecture because the customer doesn’t need the complex, enterprise-database features that Aurora offers.

As an enterprise-level database, Aurora can—with some workloads—deliver up to five times the throughput of MySQL and up to three times the throughput of PostgreSQL without requiring changes to most of your existing applications.

Aurora includes a high-performance storage subsystem. Its MySQL-compatible and PostgreSQL-compatible database engines are customized to take advantage of that fast, distributed storage. The underlying storage grows automatically as needed. An Aurora cluster volume can grow to a maximum size of 128 tebibytes (TiB). Aurora also automates and standardizes database clustering and replication, which are typically among the most challenging aspects of database configuration and administration.

Aurora is part of the managed database service Amazon Relational Database Service (Amazon RDS). Amazon RDS is a web service that makes it easier to set up, operate, and scale a relational database in the cloud. Aurora Serverless v2is an on-demand, automatic scaling configuration for Aurora.

Aurora Serverless v2 helps automate the processes of monitoring the workload and adjusting the capacity for your databases. Capacity is adjusted automatically based on application demand. You're charged only for the resources that your database clusters consume. Thus, Aurora Serverless v2 can help you to stay within budget and reduce the need to pay for computer resources that you don't use.

This type of automation is especially valuable for multitenant databases, distributed databases, development and test systems, and other environments with highly variable and unpredictable workloads.

-   For more information on Amazon Aurora Serverless, see [Using Aurora Serverless v2](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.html).
-   For links to tutorials for Amazon Aurora, see [Getting started with Amazon Aurora](https://aws.amazon.com/rds/aurora/getting-started/).

## Amazon RDS Proxy

By using Amazon RDS Proxy, your applications can pool and share database connections to improve their ability to scale. RDS Proxy makes applications more resilient to database failures by automatically connecting to a standby DB instance, while preserving application connections. By using RDS Proxy, you can also enforce AWS Identity and Access Management (IAM) authentication for databases, and securely store credentials in AWS Secrets Manager.

With RDS Proxy, you can handle unpredictable surges in database traffic that otherwise might cause issues because of oversubscribing connections or creating new connections at a fast rate. RDS Proxy establishes a database connection pool and reuses connections in this pool without the memory and CPU overhead of opening a new database connection each time. To protect the database against oversubscription, you can control the number of database connections that are created.

RDS Proxy queues or throttles application connections that can't be served immediately from the pool of connections. Although latencies might increase, your application can continue to scale without abruptly failing or overwhelming the database.

-   For more information about Amazon RDS Proxy, see [Using Amazon RDS Proxy.](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-proxy.html)

## Amazon DynamoDB

Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. By using DynamoDB, you can offload the administrative burdens of operating and scaling a distributed database so that you can reduce your need to handle hardware provisioning, setup and configuration, replication, software patching, or cluster scaling. DynamoDB also offers encryption at rest, which reduces your operational burden and the complexity involved in protecting sensitive data.

With DynamoDB, you can create database tables that can store and retrieve virtually any amount of data and serve virtually any level of request traffic. You can scale up or scale down your tables' throughput capacity with minimal downtime or performance degradation.

If you are an application developer, you might have some experience using a relational database management system (RDBMS) and Structured Query Language (SQL). As you begin working with Amazon DynamoDB, you will encounter many similarities, but also many things that are different.

_NoSQL_ is a term used to describe nonrelational database systems that are highly available, scalable, and optimized for high performance. Instead of the relational model, NoSQL databases (such as DynamoDB) use alternate models for data management, such as key-value pairs or document storage.

In DynamoDB, tables, items, and attributes are the core components that you work with. A table is a collection of items, and each item is a collection of attributes. DynamoDB uses primary keys to uniquely identify each item in a table, and secondary indexes to provide more querying flexibility. You can use DynamoDB Streams to capture data modification events in DynamoDB tables.

-   For more information about Amazon DynamoDB, see [What is Amazon DynamoDB?](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html) or [Amazon DynamoDB FAQs](https://aws.amazon.com/dynamodb/faqs/).
-   For more information about Amazon DynamoDB data modeling, see [Example of modeling relational data in DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/bp-modeling-nosql-B.html).
-   For hands-on learning with Amazon DynamoDB, see [Hands-on labs for DynamoDB](https://amazon-dynamodb-labs.com/hands-on-labs.html).
