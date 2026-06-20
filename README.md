# 🚀 Microsoft Fabric End-to-End Medallion Data Platform

A production-style Microsoft Fabric Data Engineering project implementing the Medallion Architecture (Bronze, Silver, Gold) to ingest, transform, and serve data from multiple sources, including SQL Server and Excel, powering enterprise-grade Power BI reporting.

📌 Project Overview

This project demonstrates the design and implementation of an end-to-end data platform using Microsoft Fabric. The solution follows the Medallion Architecture pattern to ingest raw data from multiple sources, transform it into analytics-ready datasets, and serve business users through Power BI dashboards.

The platform is built to be:

Scalable
Automated
Reliable
Easy to monitor
Enterprise-ready

🎯 Business Scenario
A client currently uses Excel-based reports and wants to modernize their analytics platform using Microsoft Fabric.

Requirements
Ingest data from: SQL Server (On-Premises) & Excel Files
Implement Medallion Architecture
Automate daily data refresh
Build Power BI reports
Create reusable Semantic Models
Implement monitoring and alerting
Support multiple business teams with governed access

🏗️ Solution Architecture

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/8b4d84e8-c816-4da9-a594-2dd1e6007c76" />

🏅 Medallion Architecture
Bronze Layer

Purpose:

Store raw source data
Preserve source integrity
Maintain historical records

Activities:

SQL Server ingestion
Excel ingestion
Initial metadata capture

Storage:

Fabric Lakehouse
Silver Layer

Purpose:

Data cleansing
Standardization
Validation

Activities:

Remove duplicates
Handle null values
Standardize data types
Apply business rules

Storage:

Fabric Warehouse
Gold Layer

Purpose: Business-ready analytics layer

Activities:

Aggregations
KPI calculations
Reporting datasets
Star schema optimization

Storage: Fabric Warehouse

🔧 Technologies Used
Technology	Purpose
Microsoft Fabric	Unified Analytics Platform
Dataflow Gen2	Data Ingestion
Data Pipelines	Orchestration
OneLake	Storage
Lakehouse	Bronze Layer
Warehouse	Silver & Gold Layers
Semantic Model	Data Modeling
Power BI	Reporting
SQL Server	Source System
Excel	Source System
On-Premises Gateway	Connectivity

📂 Data Sources
Source 1: SQL Server
AdventureWorks Database
Customer Data
Sales Data
Product Data
Geography Data
Source 2: Excel Files
Sales Reports
Customer Information
Product Information

⚙️ Data Ingestion Approaches
Method 1: Dataflow Gen2

Used for:
Excel ingestion
Lightweight transformations
Rapid development

Method 2: Fabric Data Pipeline

Used for:
SQL Server ingestion
Batch processing
Scheduled execution
Automated orchestration

🔄 Pipeline Workflow
Step 1:

Extract data from:
SQL Server
Excel Files

Step 2:

Load raw data into:
Bronze Lakehouse

Step 3:

Apply cleansing and validation:
Silver Warehouse

Step 4:

Create reporting datasets:
Gold Warehouse

Step 5: Build Semantic Model

Step 6: Refresh Power BI Reports

Step 7: Send alerts if refresh fails

📊 Semantic Model
The Semantic Model acts as the business layer between the Gold Warehouse and Power BI.

Benefits:

Reusable business logic
Consistent KPIs
Simplified report development
Centralized governance
📈 Reporting Layer

Power BI dashboards provide:

Sales Analytics
Total Revenue
Total Orders
Sales by Region
Sales by Product Category
Customer Analytics
Customer Segmentation
Geographic Analysis
Product Analytics
Product Performance
Category Trends
⏰ Scheduling & Automation

The solution uses Fabric Pipelines to:

Execute daily refreshes
Trigger transformations
Update Semantic Models
Refresh Power BI Reports
Schedule Daily 06:00 AM

🚨 Monitoring & Alerting:

Implemented monitoring capabilities include:
Pipeline Failure Alerts
Data Refresh Monitoring
Execution Logs
Data Quality Validation

Benefits:

Faster issue resolution
Reduced downtime
Improved reliability
🔐 Security

Implemented security controls:

Role-Based Access Control (RBAC)
Semantic Model Permissions
Workspace Security
Gateway Authentication

📊 Key Features:

✅ Multi-source data ingestion

✅ Medallion Architecture

✅ Fabric Lakehouse

✅ Fabric Warehouse

✅ Dataflow Gen2

✅ Data Pipelines

✅ Semantic Models

✅ Power BI Reporting

✅ Automated Refresh

✅ Monitoring & Alerting

✅ On-Premises Connectivity

📈 Business Benefits
Reduced manual reporting effort
Faster data availability
Improved data quality
Centralized analytics platform
Scalable architecture
Enterprise-grade governance
🚀 Future Enhancements
Incremental Loading
CDC Implementation
Real-Time Streaming
Data Quality Framework
CI/CD Deployment
Fabric Notebooks Integration
Machine Learning Integration

👨‍💻 Author

Abhishek Paul

Senior Associate | Data Engineer

Skills: Microsoft Fabric, Azure Data Factory, Databricks, PySpark, SQL, Power BI, Data Engineering

## Acknowledgements

This project was built as part of my hands-on learning journey with Microsoft Fabric, following concepts demonstrated in the VJ Tech Talks Microsoft Fabric Project Series. Additional enhancements, documentation, architecture design, and implementation details were customized and extended beyond the original tutorial.
