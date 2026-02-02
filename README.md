# hsbc-retail-banking-modern-data-platform-fabric

This project demonstrates an end-to-end modern data platform built using Microsoft Fabric for a global retail banking use case (HSBC – Retail Banking).

The objective is to showcase how Microsoft Fabric can be used to unify batch, streaming, analytics, and BI workloads into a single governed platform, enabling faster and more reliable data-driven decision making.

⚠️ Note: All data used in this project is synthetic and anonymized, created purely for architectural and POC purposes.

Business Problem Statement

HSBC Retail Banking faces the following challenges:

Fragmented data across core banking, CRM, digital channels, and fraud systems

Delayed reporting and lack of near real-time insights

Inconsistent KPIs across teams

High operational cost due to tool sprawl

Governance, lineage, and compliance gaps

The bank needs a scalable, governed, and cost-efficient analytics platform to support:

Customer 360

Retail KPIs

Fraud monitoring

Digital adoption analytics

Executive decision dashboards

🧱 Solution Architecture (Microsoft Fabric)

The solution is built using Microsoft Fabric unified SaaS architecture, leveraging:

OneLake as the single data foundation

Lakehouse for medallion architecture (Bronze / Silver / Gold)

Fabric Data Pipelines for ingestion

Event Streams for near real-time data

Spark & SQL for transformations

Power BI Semantic Models for analytics

🥉🥈🥇 Medallion Architecture
🥉 Bronze Layer – Raw Ingestion

Source-aligned raw tables

Schema-on-read

No transformations

Supports reprocessing & audit

Sources simulated:

Customer Master (CRM – Cloud)

Account Master (Core Banking – On-Prem)

Transactions (Payments – Near Real-Time)

Loans (Loan Management System)

Digital Events (Mobile / Net Banking)

Fraud Alerts (Streaming)

🥈 Silver Layer – Cleansed & Conformed

Data quality rules applied:

Deduplication

Standardization (gender, country, flags)

Null handling & defaulting

Referential integrity checks

Business-ready conformed schemas

This layer represents trusted enterprise data.

🥇 Gold Layer – Curated Analytics Models

Dimensional modeling (Star Schema) optimized for analytics and BI.

Dimensions

dim_customer (SCD-ready)

dim_account

dim_date

dim_channel

Facts

fact_transactions

fact_customer_daily

fact_loan_portfolio

fact_fraud

These tables power executive dashboards and self-service analytics.

👥 Target Users
Role	Usage
CXOs & Leadership	Strategic KPIs
Retail Business Heads	Growth & performance
Branch Managers	Targets & branch KPIs
Risk & Compliance	NPA & regulatory metrics
Fraud Teams	Near real-time alerts
Data Analysts	Self-service analysis
Data Engineers	Pipelines & transformations
📊 Key KPIs Enabled

Customer acquisition & churn

Transaction volume & success rate

Digital adoption trends

Loan portfolio & NPA %

Fraud rate & detection latency

Branch vs digital performance

🔐 Security & Governance

Role-based access control (RBAC)

Row-level security (Country / Branch)

End-to-end lineage (Source → Report)

Centralized data catalog

Audit-ready architecture

📁 Repository Structure
├── bronze/
│   └── raw_tables.sql
├── silver/
│   └── cleansing_transformations.sql
├── gold/
│   ├── dimensions.sql
│   └── facts.sql
├── pipelines/
│   └── fabric_data_pipelines.md
├── semantic-model/
│   └── powerbi_model.md
├── powerbi/
│   └── dashboard_screenshots/
├── docs/
│   ├── architecture_overview.md
│   └── poc_scope.md
└── README.md

🚀 POC Success Criteria

This POC demonstrates:

End-to-end Fabric implementation

Medallion architecture best practices

Scalable dimensional modeling

Near real-time analytics capability

Enterprise governance & security

Cost-efficient unified analytics platform

🧠 Why Microsoft Fabric

Unified analytics (no tool sprawl)

Tight Power BI integration

OneLake reduces data duplication

Built-in governance & lineage

Faster time-to-value for business users

🏁 Conclusion

This project represents a real-world, enterprise-grade Microsoft Fabric implementation for retail banking, designed from a Data Architect’s perspective.

It can be extended further to include:

Machine Learning models

CI/CD automation

Data quality frameworks

Domain-driven data products

👤 Author

Data Architect / BI Architect
Specializing in:

Microsoft Fabric

Modern Data Platforms

Retail Banking Analytics

Enterprise BI & Governance
