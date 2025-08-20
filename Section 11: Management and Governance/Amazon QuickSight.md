# Amazon QuickSight – AWS MLE-A Notes

## Overview
- 📊 **QuickSight** = AWS’s BI & visualization tool (like Tableau/PowerBI).  
- 🌐 Serverless, browser/mobile-based, scalable to 100k+ users.  
- 🎯 Targeted at **business users** (not developers).  

## Data Sources
- 🔗 AWS: Redshift, RDS, Aurora, Athena, S3 (data lakes), IoT Analytics.  
- 🔗 External: On-prem DBs, EC2-hosted DBs, Excel/CSV/TSV/log files, Salesforce, JDBC/ODBC.  
- ⚙️ Some **basic data prep/transform** (rename columns, calculated fields, type casting).  
- 🚫 Not designed for **heavy ETL** (use Glue for that).  

## Engine – SPICE ⚡
- **SPICE** = Super-fast Parallel In-memory Calculation Engine.  
- 🗂️ Columnar storage, machine code generation.  
- 🚀 Enables **interactive queries on big data**.  
- Limit: 10 GB per user.  

## Use Cases
- 📊 Dashboards & KPI reports.  
- 🔎 Ad hoc data exploration.  
- 📝 Paginated Reports (multi-page printable reports).  
- 🔥 Log analysis on data in S3/Redshift/Athena.  

## Machine Learning Features
- 🤖 **ML Insights**:  
  - Anomaly Detection (Random Cut Forest).  
  - Forecasting (seasonality, trends, outlier removal).  
  - Auto Narratives (plain-language insights in dashboards).  
- 🗣️ **QuickSight Q**: Natural Language Queries.  
  - “Top selling items in Florida?”  
  - Requires **data prep** (NLP-friendly names, topics).  
  - Add-on feature, extra cost.  

## Security
- 🔐 MFA, IAM integration, SAML/SSO, AD integration (Enterprise Edition).  
- 🧑‍🤝‍🧑 Row-Level Security (RLS) → restrict access to rows of data.  
- 📑 Column-Level Security (Enterprise only).  
- 🔒 Private VPC access via ENI / Direct Connect.  

## User Management
- 👥 IAM-based or email signup.  
- 📧 Enterprise edition: SAML SSO, AD integration.  
- 💰 Charged per user → must manage users carefully.  

---

## 🔑 Exam Tips
- 🖼️ QuickSight = BI tool → dashboards, KPI reports, ad hoc exploration.  
- ⚡ SPICE engine = super-fast queries, **10 GB/user limit**.  
- 🤖 ML Insights = anomaly detection + forecasting (uses RCF).  
- 🗣️ QuickSight Q = NLP queries → needs **data prep**.  
- 🚫 Not for ETL → use Glue instead.  
- 🔐 RLS & CLS (Enterprise only for column-level).  
- 📑 Paginated reports = printable management reports.  

---
