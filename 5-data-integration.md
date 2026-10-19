# 4 - Data Integration <!-- omit in toc -->

## Contents <!-- omit in toc -->

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

# 4. Manual Data Integration

- **Pros**
  - Low cost.
  - Total control.
- **Cons**
  - Difficult to scale.
  - Human error.

## 4.1. Middleware Data Integration

- **Pros**
  - Better data streaming.
  - Easier access between systems.
- **Cons**
  - Maintenance.
  - Limited functionality.

## 4.2. Application Based Integration

- **Pros**
  - Simplified processes.
  - Easier information exchange.
  - Fewer resources used.
- **Cons**
  - Maintenance.
  - Inconsistent results.
  - Complicated setup.
  - Difficult data management.

## 4.3. Uniform access Integration

- **Pros**
  - Lower storage requirements.
  - Easier data access.
  - Simplified view of data.
- **Cons**
  - Data integrity challenges.
  - Strained systems.

## 4.4. Common Storage Integration (Data Warehouse)

- **Pros**
  - Reduced burden.
  - Increased data version management control.
  - Cleaner data.
  - Enhanced data analytics.
- **Cons**
  - Increased storage costs.
  - Higher maintenance costs.

## 4.5. Data Virtualization

- **Pros**
  - No need to move data.
  - Scalable.
  - No need to maintain data in multiple locations.
- **Cons**
  - Cost

# 5. ETL

![ETL Process](/images/etl-process.png)

# 6. ELT

TODO: DIAGRAM

# 7. ETL vs ELT

- **Pros of ETL**
  - **Compliance: ** ETLis better for compliance with GDPR, HIPAA, CCPA.
  - **Implementation:** Many ETL tools and experts.
  - **Maturity:** More documentation, tools and best practices.
- **Pros of ELT**
  - **Maintenance:** All data is always flowing with automated process.
  - **Speed:** Data available in Data Warehouse faster since no transformation layer.
  - **Cost:** Only cloud-based platforms needed at lower cost, on-premise ETL processes require expensive hardware.

# 8. Data Integration Tools

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

# 9. Data Integration Best Practices

1. Identify your business needs first
2. Include internal business expert in the data integration team
3. Consider Long-Term Goals
4. Take into consideration the total cost of all methods
5. Avoid very complex data integration solutions
6. Choose a flexible solution
