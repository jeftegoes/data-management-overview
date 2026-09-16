# 1 - Data Architecture <!-- omit in toc -->

## Contents <!-- omit in toc -->

- [1. What is Data Architecture](#1-what-is-data-architecture)
- [2. Data Architecture components](#2-data-architecture-components)
- [3. Data Architecture frameworks](#3-data-architecture-frameworks)
- [4. Foundational Structural Paradigms](#4-foundational-structural-paradigms)
  - [4.1. Centralized Data Architecture](#41-centralized-data-architecture)
  - [4.2. Federated Data Architecture](#42-federated-data-architecture)
  - [4.3. Distributed Data Architecture](#43-distributed-data-architecture)
- [5. Functional Orientation of Architecture](#5-functional-orientation-of-architecture)
  - [5.1. Operational Data Architecture (OLTP)](#51-operational-data-architecture-oltp)
  - [5.2. Analytical Data Architecture (OLAP)](#52-analytical-data-architecture-olap)
  - [5.3. How OLTP and OLAP Work Together](#53-how-oltp-and-olap-work-together)
- [6. Data Storage \& Integration Patterns](#6-data-storage--integration-patterns)
  - [6.1. Data Warehouse Architecture](#61-data-warehouse-architecture)
  - [6.2. Data Lake \& Data Lakehouse Architectures](#62-data-lake--data-lakehouse-architectures)
- [7. Modern Enterprise Evolution Patterns](#7-modern-enterprise-evolution-patterns)
  - [7.1. Data Mesh Architecture](#71-data-mesh-architecture)
  - [7.2. Data Fabric Architecture](#72-data-fabric-architecture)
- [8. Data Architecture best practices](#8-data-architecture-best-practices)

# 1. What is Data Architecture

- "Data architecture is a set of rules, policies, standards and models that govern and define the type of data collected and how it is used, stored, managed and integrated within an organization and its database systems. It provides a formal approach to creating and managing the flow of data and how it is processed across an organization's IT systems and applications".

# 2. Data Architecture components

1. Data pipelines.
2. Cloud storage.
3. Cloud computing.
4. AI and ML models.
5. Data streaming.
6. Container orchestration.
7. Real-time analytics.

# 3. Data Architecture frameworks

1. DAMA-DMBOK-2.
2. Zachman Framework for Enterprise Architecture.
3. The Open Group Architecture Framework (TOGAF).

# 4. Foundational Structural Paradigms

- How your enterprise organizes and governs its data ecosystem.

| Centralized        | Federated                | Distributed                   |
| ------------------ | ------------------------ | ----------------------------- |
| One hub, one model | Semi-independent domains | Multi-node, synchronized data |
| Strong governance  | Shared standards         | High scalability              |

## 4.1. Centralized Data Architecture

- _Designing for consistency and control._
- **Core Idea**
  - All enterprise data managed in a single unified environment – one source of truth
- **Key Features**
  - Central data warehouse or hub.
  - Standardized models &-metadata.
  - Enterprise-wide governance.
- **Benefits**
  - Data consistency.
  - Easier quality control.
  - Unified analytics.
- **Challenges**
  - Slower adaptability.
  - Central IT bottlenecks.
- _Use for stable, highly regulated organizations._

## 4.2. Federated Data Architecture

- _Balancing autonomy and integration._
- **Core Idea**
  - Data management is decentralized across domains with local control; enterprisevide interoperapility via shared standards.
- **Key Features**
  - Domain-owned data platforms.
  - Shared metadata & common semantics.
  - Standardized interfaces (APIs/events) for data exchange.
- **Benefits**
  - Local autonomy & speed.
  - Scales with organization growth.
  - Resilient to change.
- **Challenges**
  - Cross-domain consistency.
  - Integration complexity.
  - Use for diverse, multi-domain enterprises or multi-region operations.

## 4.3. Distributed Data Architecture

- _Scale out with resilience and locality._
- **Core Idea**
  - Data and compute spread across nodes/regions with coordinated consistency; logial unity through physical distributions.
- **Key Features**
  - Partitioning/sharding.
  - Replication.
  - Consensus protocols.
  - Multi-region leader/follower; geo-routing.
  - Conflict resolution.
- **Challenges**
  - Consistency trde-offs (CAP, PACELC).
  - Complexity of orchestration.
  - Cross-region write conflicts.
  - Data governance & schema consistency.
- **Use for:** Global platforms, IoT/edge, high-throughput streaming.

# 5. Functional Orientation of Architecture

- Designing for the workload: transactions vs insights.

  | Operational (OLTP)     | Analytical (OLAP)         |
  | ---------------------- | ------------------------- |
  | Real-time transactions | Strategic decision-making |
  | Normalized schema      | Dimensional schema        |
  | High frequency writes  | Heavy read aggregates     |

## 5.1. Operational Data Architecture (OLTP)

- _Supporting real-time business processes._
- **Core Idea**
  - Handles daily transactions - capturing and updating operational data.
- **Key Components**
  - Operational databases (RDBMS).
  - ODS / MDM systems.
  - APIs for applications.
- **Principles**
  - Normalized schema.
  - ACID compliance.
  - Fast reads/writes.
- **Think:** Order systems, payments, CRM transactions.

## 5.2. Analytical Data Architecture (OLAP)

- _Turning data into enterprise insight._
- **Core Idea**
  - Structured for data analysis, reporting, and decision-making.
- **Main Components**
  - Data warehouse & marts.
  - ETL/ELT pipelines.
  - BI and visualization tools.
- **Design Patterns**
  - **Kimball:** dimensional (star/snowflake).
  - **Inmon:** Normalized enterprise view.
- Supports KPIs, dashboards, predictive analytics.

## 5.3. How OLTP and OLAP Work Together

- Running the business vs. Understanding the business.
- **Operational Data Architecture (OLTP)**
  - **Purpose:** Runs day-to-day operations.
  - **Focus:** Real-time transactions.
  - **Data Type:** Current, detailed, frequently updated.
  - **Examples:** Order systems, CRM, payment processing.
- **How They Connect**
  - -> ETL / ELT pipelines.
  - -> Change Data Capture (CDC).
  - -> Streaming or data integration tools.
  - Keeps business running efficiently and learning continuously.
- **Analytical Data Architecture (OLAP)**
  - **Purpose:** Supports decision-making
  - **Focus:** Historical analysis & performance insights
  - **Examples:** Aggregated, structured, historical
  - **Answers:** "Why is this happening?" and "What should we do next?"
- **Modern Trend: HTAP (Hybrid Transactional/Analytical Processing)**
  - Combine OLTP + OLAP on same platform.
  - Enables real-time analytics on live data.

# 6. Data Storage & Integration Patterns

- _Where data lives, how it's shaped, and how it flows._
- **Warehouse** -> Curated, schema-on-write.
- **Data Lake** -> Flexible, schema-on-read.
- **Lakehouse** -> Unified, ACID-enabled.

## 6.1. Data Warehouse Architecture

- _Integrating data for consistent analytics_.
- **Core Idea**
  - A structured system to consolidate and organize enterprise data.
- **Architectural Layers**
  - Staging → Integration → Presentation.
  - Metadata & governance overlay.
- **Approaches**
  - Kimball: bottom-up.
  - Inmon: top-down.
  - Data Vault 2.0: agile, auditable.
- Cloud warehouses (Snowflake, BigQuery) modernize this model.

## 6.2. Data Lake & Data Lakehouse Architectures

- **From raw data pools to governed intelligence**.
- **Core Idea**
  - Data lakes store diverse, raw data; lakehouses add structure + ACID reliability.
- **Data Lake**
  - Flexible, schema-on-read.
- **Lakehouse**
  - Adds schema-on-write & transactions.
- **Tech Stack**
  - Delta Lake.
  - Apache Iceberg.
  - Apache Hudi.
- Best for mixed workloads & open data ecosystems.

# 7. Modern Enterprise Evolution Patterns

- The future of large-scale, intelligent data ecosystems.
- **Data Mesh**
  - Organizational model.
  - Domains own & publish **data products**.
  - "Data as a product" mindset.
- **Data Fabric**
  - Technological layer.
  - **Active metadata**, automation, knowledge graph.
  - Intelligent integration across all systems.
- **Together**
  - Mesh = _Who_ owns data.
  - Fabric = _How_ data connects.

## 7.1. Data Mesh Architecture

- _Organizing data around business domains_.
- **Core Idea**
  - Data managed decentrally by domain teams - "data as a product.".
- **Four Principles**
  1. Domain ownership.
  2. Data as a product.
  3. Self-serve platform.
  4. Federated governance.
- **Outcome**
  - Scalable, collaborative data ecosystems.
- Great for large enterprises embracing agile, domain-driven design.

## 7.2. Data Fabric Architecture

- _Intelligent connectivity across the enterprise_.
- **Core Idea**
  - An AI- and metadata-driven integration layer connecting all data sources seamlessly.
- **Core Components**
  - Metadata management.
  - Knowledge graphs.
  - Automated governance & discovery.
- **Benefits**
  - End-to-end visibility.
  - Faster data delivery.
  - Unified access without migration.
- Complements Data Mesh - Tech layer enabling global integration.

# 8. Data Architecture best practices

1. Cloud-native.
2. Robust and scalable data pipelines.
3. Seamless data integration.
4. Real-time data enablement.
5. Decoupled and extensible.
6. Domain-driven.
7. Balanced.
