# 🧪 AWS Glue – Cheat Sheet (MLE-A Exam)

## 🔍 What is AWS Glue?
- **Serverless** data integration service for **ETL** (Extract, Transform, Load)
- Automatically discovers schema from **unstructured data in S3**
- Connects S3 data lakes to analytics tools like:
  - Amazon Athena
  - Amazon Redshift Spectrum
  - Amazon EMR (Hive, Spark)
  - Amazon QuickSight

---

## ⚙️ Key Components

| Component         | Purpose                                                                 |
|------------------|-------------------------------------------------------------------------|
| **Glue Crawler** | Scans S3 data, infers schema, and populates the Glue Data Catalog       |
| **Data Catalog** | Central metadata repository; stores table definitions for S3 data       |
| **ETL Jobs**     | Runs data transformations using **Apache Spark** (no cluster to manage) |

---

## 🧠 Exam Tips

- Glue is **fully managed & serverless** – no infra to maintain
- Schema discovery makes **S3 data queryable like SQL tables**
- Glue **ETL jobs** can be triggered **on schedule, on demand, or by events**
- **Apache Spark** is used under the hood, but **you don’t manage it**

---

## 📦 S3 Partitioning Strategy

### ✅ Partition for performance:
Helps reduce scan size and speed up queries in Athena/Redshift.

### Example 1: Query by time  
Structure:  
