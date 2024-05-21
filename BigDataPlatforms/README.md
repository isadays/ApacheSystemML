# BigDataPlatforms


Apache Hadoop writes intermediate data to disk. It distributes work across multiple nodes. It is an implementation of Map Reduce.

Apache Spark - distributed computation - is a big data analytics engine. It uses RAM memory. Generally faster than Hadoop (for iterative work). Attaches to several cluster management systems. 


### Choosing between Hadoop and Spark

 Hadoop might be preferred for batch processing, while Spark is more suitable for real-time processing and versatile analytics.

Spark's easier APIs might be appealing if you're starting fresh.

Infrastructure: Consider your existing infrastructure. If you have a Hadoop cluster in place, it might make sense to continue leveraging it. Spark's speed advantage can be crucial for time-sensitive applications, but Hadoop's ecosystem might be preferred for certain tasks.

### Resilient Distributed Datasets (RDDs) : Transformations (lazy) and Actions(immediate computationn)

Fundamental data structure in the Apache Spark framework, designed to facilitate distributed data processing across clusters. Foundational building blocks for Spark applications, enabling fault-tolerant, parallelized data processing in a distributed computing environment.

- Resilience: RDDs are "resilient" because they can recover from node failures. Through lineage information, Spark can recreate lost data partitions by recomputing them from the original data and transformations.

- Distributed: RDDs are distributed across multiple nodes in a Spark cluster, allowing for parallel processing of data. Each RDD is divided into partitions, with each partition residing on a separate node.

The file RDD.ipynb contains an RDD in spark. 
- Immutable: RDDs are immutable, meaning their content cannot be changed once created. Instead, transformations applied to RDDs produce new RDDs, preserving data integrity.

- In-Memory Processing: RDDs are stored in memory, enabling faster data access and computation compared to traditional disk-based storage. This in-memory processing contributes to Spark's speed advantage.

- Transformation and Action Operations: RDDs support two types of operations: transformations (e.g., map, filter, reduceByKey), which create new RDDs from existing ones, and actions (e.g., count, collect, saveAsTextFile), which trigger computations and return results.

 - Data Partitioning: RDDs allow users to control data partitioning, which can optimize data locality and enhance processing efficiency.

### Spark SQL : Module for structured data processing. 

Structured Data Processing: CSV, Parquet, JSON, and relational databases, using SQL queries. This enables a familiar SQL-based approach for querying and analyzing data.

DataFrames: Spark SQL introduces DataFrames, which are distributed collections of data organized into named columns. DataFrames provide a higher-level abstraction compared to RDDs (Resilient Distributed Datasets) and are optimized for structured data manipulation.  It is a Dataset with named columns. It is a table-like structure. It has the capabilities of an RDD enhanced with Spark Sql optimizations.

Schema Inference and Evolution: Spark SQL can automatically infer the schema of structured data sources, making it easy to work with data without defining a schema explicitly. It also supports schema evolution, allowing changes to the schema as data evolves.

Interoperability: Spark SQL integrates with other Spark components, such as Spark Streaming, Spark MLlib, and Spark GraphX. This integration enables end-to-end data processing pipelines encompassing data ingestion, transformation, analysis, and machine learning.

Hive Compatibility: Spark SQL is fully compatible with Apache Hive, a popular data warehousing tool. Users can run Hive queries and migrate existing Hive workloads to Spark SQL with minimal code changes.

Optimization: Spark SQL performs various optimizations, including predicate pushdown, column pruning, and constant folding, to optimize query performance. It leverages Spark's Catalyst query optimizer and Tungsten execution engine.

User-Defined Functions (UDFs): Users can define custom functions in Spark SQL, including User-Defined Aggregation Functions (UDAFs) and User-Defined Scalar Functions (UDFs), to extend SQL capabilities.

Streaming Support: Spark SQL can process structured streaming data, allowing real-time processing of data streams using SQL queries and DataFrames.


### Differences between Spark SQL and PySpark. 

Spark SQL: Spark SQL is a module in Apache Spark that provides a SQL interface for working with structured and semi-structured data. It allows you to run SQL queries on structured data, much like a traditional relational database. Primarily used for querying and analyzing structured data stored in various formats such as Parquet, Avro, ORC, JSON, CSV, and relational databases. It's ideal for data exploration, transformation, and reporting tasks. Spark SQL is not tied to any specific programming language. You can use it with Scala, Java, Python (PySpark), and R to execute SQL queries and work with DataFrames.

PySpark:  Python library for Apache Spark. It provides a Python API to interact with Spark's core functionality, including distributed data processing, machine learning, and graph processing. PySpark is a versatile library used for various tasks, such as ETL (Extract, Transform, Load) operations, data preprocessing, running machine learning algorithms, and more. It's particularly popular among data scientists and engineers who prefer working in Python.

Integration with Spark SQL: PySpark seamlessly integrates with Spark SQL. You can use the Spark SQL module within PySpark to run SQL queries on DataFrames created using PySpark's API.


Spark SQL is a specific module within Spark that provides SQL capabilities for structured data, while PySpark is a library that allows you to use Spark with Python.

Spark SQL is used for querying structured data with SQL-like syntax, while PySpark provides a broader set of APIs for various Spark tasks, including data processing, machine learning, and more.  PySpark is more versatile and covers a wider range of Spark's functionality, while Spark SQL is focused on structured data queries.

### Snowflake is a storage and computation platform designed for big data

Runs as a service on public clouds. Storage and computation platform. Uses Snowflake SQL. 

Snowflake layers: Cloud services (interface to other layers, security and query optimization), Compute layer(clusters of nodes allocated by Snowflake from a cloud provider), storage layer (fully managed by Snowflake).

Standard and Snowpark (machine learning tasks) warehouses 

### AZURE Databricks is a cloud-based big data analytics 
