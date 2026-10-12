# 3 - Data Storage and Operations <!-- omit in toc -->

## Contents <!-- omit in toc -->

- [1. What is Data Storage and Operations](#1-what-is-data-storage-and-operations)
- [2. Benefits of good Data Storage Strategy](#2-benefits-of-good-data-storage-strategy)
- [3. Intro to Data Storage Systems](#3-intro-to-data-storage-systems)
  - [3.1. File Storage Systems](#31-file-storage-systems)
  - [3.2. Block Storage Systems](#32-block-storage-systems)
  - [3.3. Object Storage Systems](#33-object-storage-systems)
  - [3.4. Relational Databases (RDBMS)](#34-relational-databases-rdbms)
  - [3.5. Non-Relational (NoSQL) Databases](#35-non-relational-nosql-databases)
  - [3.6. Data Warehouses](#36-data-warehouses)
  - [3.7. Data Lakes](#37-data-lakes)
  - [3.8. Hybrid \& Cloud Storage Systems](#38-hybrid--cloud-storage-systems)
  - [3.9. Distributed \& Decentralized Storage](#39-distributed--decentralized-storage)
- [4. Data Storage Best Practices](#4-data-storage-best-practices)
- [5. Data Storage activities](#5-data-storage-activities)
- [6. Data Storage Management key attributes](#6-data-storage-management-key-attributes)
- [7. Data Backup, Recovery \& Archiving](#7-data-backup-recovery--archiving)
- [8. Data Storage Security \& Access Control](#8-data-storage-security--access-control)
- [9. Data Retention \& Lifecycle Management](#9-data-retention--lifecycle-management)
- [10. Performance Optimization \& Monitoring](#10-performance-optimization--monitoring)

# 1. What is Data Storage and Operations

- "Data storage and Operations includes the design, implementation, and support of stored data, to maximize its value throughout its lifecycle, from creation/acquisition to disposal".
- **Two sub-activities**
  1. Database support
  2. Databasetechnology support

# 2. Benefits of good Data Storage Strategy

1. Reduce capital expenses.
2. Reduce operational expenses.
3. Easier data management.
4. Optimized resource utilization.
5. Easier scalability.
6. Better performance.
7. Better user experience.

# 3. Intro to Data Storage Systems

- Every business needs a place to **store and organize data**.
- A storage system keeps data **safe, accessible, and ready to use**.
- Different systems are made for **different purposes** - from storing files to running analytics.

## 3.1. File Storage Systems

- Simple & Familiar - Like Your Computer Folders.
  - Saves data as **files and folders**.
  - Best for **documents, photos, videos, and logs**.
  - Easy to use but not ideal for large-scale analysis.
  - Accessed via shared network protocols like NFS or SMB.
- **Examples**
  - Windows File Server.
  - NAS.
  - HDFS.
- **Key Takeaway**
  - Great for everyday file storage - simple, familiar, and reliable.

## 3.2. Block Storage Systems

- Fast and Reliable.
  - Splits data into **small "blocks"** stored separately.
  - Very **fast** - used for databases and virtual machines.
  - Provides **low-latency and high reliability**.
- **Examples**
  - Storage Area Network (SAN).
  - Amazon EBS.
- **Key Takeaway**
  - Ideal for **high-speed, structured data** like financial systems.

## 3.3. Object Storage Systems

- Designed for the Cloud.
  - Data stored as **objects** with details and unique IDs.
  - Handles **massive amounts of unstructured data**.
  - Perfect for **backups, videos, images, and logs**.
- **Examples**
  - Amazon S3.
  - Azure Blob Storage.
  - Google Cloud Storage.
- **Key Takeaway**
  - Highly scalable - the **backbone of cloud storage** today.

## 3.4. Relational Databases (RDBMS)

- Organized & Reliable Data Storage.
  - Stores data in **tables** (like spreadsheets).
  - Uses **relationships** between data (e.g., customers ↔ orders).
  - Great for **structured data** and clear rules.
- **Examples**
  - MySQL.
  - Oracle.
  - PostgreSQL.
  - SQL Server.
- **Key Takeaway**
  - The go-to for **business applications** that need accuracy and order.

## 3.5. Non-Relational (NoSQL) Databases

- Flexible & Fast for Modern Apps.
  - No fixed tables — stores **different data formats**.
  - **Scales easily** for web, mobile, and IoT data.
  - Great for **fast-changing or large data volumes**.
- **Examples**
  - MongoDB.
  - Redis.
  - Cassandra.
  - Neo4j.
- **Key Takeaway**
  - Perfect for **social media, e-commerce, and big data apps**.

## 3.6. Data Warehouses

- For Analytics, Reporting & Insights.
  - Collects **clean, structured data** from many sources.
  - Used for **dashboards, KPIs, and reports**.
  - Optimized for **analysis**, not daily transactions.
- **Examples**
  - Snowflake.
  - Google BigQuery.
  - Amazon Redshift.
- **Key Takeaway**
  - The **brain of business intelligence** — where insights live.

## 3.7. Data Lakes

- Store Everything, Analyze Anything.
  - Holds **raw, unprocessed data** (structured & unstructured).
  - Supports **AI, ML, and exploratory analytics**.
  - Scales easily for **big data environments**.
- **Examples**
  - Hadoop.
  - Azure Data Lake.
  - AWS S3 Data Lake.
- **Key Takeaway**
  - Great for **data scientists** and large-scale analytics.

## 3.8. Hybrid & Cloud Storage Systems

- Best of Both Worlds — On-Prem + Cloud.
  - Mix of **local servers** and **cloud storage**.
  - Balances **control, cost, and scalability**.
  - Common in businesses moving gradually to the cloud.
- **Examples**
  - AWS Outposts
  - Azure Stack
  - Google Anthos
- **Key Takeaway**
  - Offers **flexibility and backup safety** for modern enterprises.

## 3.9. Distributed & Decentralized Storage

- **Next-Gen:** Shared & Secure Data Storage.
  - Data stored across **many computers or locations**.
  - Increases **security, reliability, and transparency**.
  - Used in **Web3, blockchain, and decentralized apps**.
- **Examples**
  - IPFS.
  - Storj.
  - Filecoin.
  - Sia.
- **Key Takeaway**
  - Future-ready storage that promotes **trust and decentralization**.

# 4. Data Storage Best Practices

- Utilize automated storage management tools.
- Consolidate Storage Pools
- Know your data needs
- Tiered data storage
- Disaster recovery plans

# 5. Data Storage activities

- Monitoring Hardware and Software assets
- Relocating storage resources
- Track storage activities and metrics
- Resolving performance issues
  Data Storage
  Process automation,
  memory management,
  storage provisioning
  Report on KPIs
  related to storage

# 6. Data Storage Management key attributes

- Performance.
- Reliability.
- Recoverability.
- Capacity.

# 7. Data Backup, Recovery & Archiving

- Protecting Data from Loss and Disaster.
  - Every organization needs a **backup plan** — data loss can happen anytime.
  - Backups ensure data can be **recovered quickly** after failures or cyberattacks.
- **Three main backup types**
  - _Full Backup_ - a complete copy of all data
  - _Incremental Backup_ - only changes since the last backup
  - _Differential Backup_ - changes since the last full backup
- **Archiving** stores long-term data that's rarely accessed but must be retained.
- **Goals**
  - Reduce downtime (RTO)
  - Minimize data loss (RPO)
  - Meet compliance requirements

# 8. Data Storage Security & Access Control

- Keeping Stored Data Safe and Private.
- Data security protects against **unauthorized access, loss, or misuse**.
- **Encryption** keeps data safe:
  - _At Rest_ - protects stored data
  - _In Transit_ - protects data while it's moving
- **Access control**:
  - Role-Based Access Control (RBAC).
  - Identity and Access Management (IAM).
  - Audit logs to track who accessed what.
- Stay **compliant with regulations**:
  - GDPR
  - HIPAA
  - ISO 27001
- Security = **People + Processes + Technology** working together.

# 9. Data Retention & Lifecycle Management

- Managing Data from Creation to Deletion.
- **All data goes through a lifecycle**
  - 1 Creation
  - 2 Usage
  - 3 Storage
  - 4 Archiving
  - 5 Deletion
- Retention policies define how long data should be kept.
- **Lifecycle management automates movement between storage tiers**
  - _Hot Storage_: frequently used data.
  - _Warm Storage_: accessed occasionally.
  - _Cold Storage_: long-term archives.
- **Benefits**
  - Saves cost.
  - Improves performance.
  - Ensures compliance.

# 10. Performance Optimization & Monitoring

- Keeping Storage Systems Fast and Efficient.
- **Key metrics to monitor**
  - _IOPS_ - input/output operations per second.
  - _Latency_ - delay between request and response.
  - _Throughput_ - total data moved per second.
- **Techniques to improve performance**
  - Caching.
  - Data compression.
  - Deduplication.
  - Load balancing.
- **Monitoring tools**
  - Prometheus, Grafana, AWS CloudWatch.
- Regular optimization keeps systems healthy and responsive.
