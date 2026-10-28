# 5 - Data Integration <!-- omit in toc -->

## Contents <!-- omit in toc -->

- [1. What is Data Integration](#1-what-is-data-integration)
  - [1.1. Example of Data Integration](#11-example-of-data-integration)
- [2. Importance of Data Integration](#2-importance-of-data-integration)
- [3. Techniques for Data Integration](#3-techniques-for-data-integration)
  - [3.1. Manual Data Integration](#31-manual-data-integration)
  - [3.2. Middleware Data Integration](#32-middleware-data-integration)
  - [3.3. Application Based Integration](#33-application-based-integration)
  - [3.4. Uniform access Integration](#34-uniform-access-integration)
  - [3.5. Common Storage Integration (Data Warehouse)](#35-common-storage-integration-data-warehouse)
  - [3.6. Data Virtualization](#36-data-virtualization)
- [4. ETL vs ELT](#4-etl-vs-elt)
  - [4.1. ETL](#41-etl)
  - [4.2. ELT](#42-elt)
  - [4.3. Pros](#43-pros)
- [5. Data Integration Tools](#5-data-integration-tools)
- [6. Data Integration Best Practices](#6-data-integration-best-practices)

# 1. What is Data Integration

- "Data Integration is the process of consolidating data from different sources into one, unified view for efficient data management".

## 1.1. Example of Data Integration

- **Company A** uses the following:
  - Salesforce for customer information and sales pipeline data.
  - External vendor for additional customer firmographics.
  - Internal database that tracks customer satisfaction ratings from surveys.
  - Internal financial system that tracks the sales revenue per customer.
  - Marketing department database on customer campaigns.
  - **Goal:** Integration all the above sources into single source!

# 2. Importance of Data Integration

- Complete view of business intelligence, insights and analytics.
- Increased efficiency and ROI - no need for manual data gathering.
- Better employee, customer and partner experience.
- Improves Collaboration.
- Eliminates Data Silos.
- Reduces errors.
- Faster innovation, sales, time to market.
- Improves Data Quality and Integrity.

# 3. Techniques for Data Integration

- Manual Data Integration.
- Middleware Data Integration.
- Application Based Integration.
- Uniform Access Integration.
- Common Storage Integration (Data Warehousing).
- Data Virtualization.

## 3.1. Manual Data Integration

- **Pros**
  - Low cost.
  - Total control.
- **Cons**
  - Difficult to scale.
  - Human error.
- **Practical Example:** A small e-commerce store where a financial analyst downloads weekly sales reports as CSV files from the e-commerce platform (such as Shopify), opens them in Excel, copies and pastes the values into a financial control spreadsheet, and manually adjusts the columns to consolidate revenue.

## 3.2. Middleware Data Integration

- **Pros**
  - Better data streaming.
  - Easier access between systems.
- **Cons**
  - Maintenance.
  - Limited functionality.
- **Practical Example:** A digital bank that uses a message queue system such as Apache Kafka or RabbitMQ.
  - When a customer performs a transaction, an event is sent to the middleware, which immediately distributes it to notification systems, fraud detection services, and statement updates.

## 3.3. Application Based Integration

- **Pros**
  - Simplified processes.
  - Easier information exchange.
  - Fewer resources used.
- **Cons**
  - Maintenance.
  - Inconsistent results.
  - Complicated setup.
  - Difficult data management.
- **Practical Example:** A CRM system (such as Salesforce or HubSpot) integrating with a company's ERP via dedicated scripts and custom routines to synchronize newly registered customers.

## 3.4. Uniform access Integration

- **Pros**
  - Lower storage requirements.
  - Easier data access.
  - Simplified view of data.
- **Cons**
  - Data integrity challenges.
  - Strained systems.
- **Practical Example:** A corporate dashboard or portal that provides a unified interface for querying customer data.

## 3.5. Common Storage Integration (Data Warehouse)

- **Pros**
  - Reduced burden.
  - Increased data version management control.
  - Cleaner data.
  - Enhanced data analytics.
- **Cons**
  - Increased storage costs.
  - Higher maintenance costs.
- **Practical Example:** A large retail chain that consolidates data from physical store ERPs, its website, and logistics systems.
  - Every night, ETL (Extract, Transform, Load) processes extract this data, clean inconsistencies, and load it into a centralized repository such as Snowflake, Google BigQuery, or Amazon Redshift to power Power BI dashboards.

## 3.6. Data Virtualization

- **Pros**
  - No need to move data.
  - Scalable.
  - No need to maintain data in multiple locations.
- **Cons**
  - Cost
- **Practical Example:** A multinational company uses a virtualization tool like Denodo to connect directly to its local SQL databases, cloud file storage (AWS S3), and marketing APIs.
  - The virtual layer abstracts these sources, allowing data scientists to run SQL queries as if everything were stored in a single database, without moving a single gigabyte of data.

# 4. ETL vs ELT

## 4.1. ETL

![ETL Process](/images/etl-process.png)

## 4.2. ELT

![ELT Process](/images/elt-process.png)

## 4.3. Pros

- **Pros of ETL**
  - **Compliance:** ETLis better for compliance with GDPR, HIPAA, CCPA.
  - **Implementation:** Many ETL tools and experts.
  - **Maturity:** More documentation, tools and best practices.
- **Pros of ELT**
  - **Maintenance:** All data is always flowing with automated process.
  - **Speed:** Data available in Data Warehouse faster since no transformation layer.
  - **Cost:** Only cloud-based platforms needed at lower cost, on-premise ETL processes require expensive hardware.

# 5. Data Integration Tools

- **On-premise tools**
  - Oracle Data Service Integrator.
  - Informatica PowerCenter.
  - IBM InfoSphere Information Server.
- **Cloud-based tools**
  - SnapLogic.
  - Talend Cloud Integration.
- **Open-source tools**
  - Talend Open Studio.
  - Tibco Jaspersoft.

# 6. Data Integration Best Practices

1. Identify your business needs first.
2. Include internal business expert in the data integration team.
3. Consider Long-Term Goals.
4. Take into consideration the total cost of all methods.
5. Avoid very complex data integration solutions.
6. Choose a flexible solution.
