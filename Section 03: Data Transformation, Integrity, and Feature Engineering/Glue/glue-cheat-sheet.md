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
s3://bucket/year=2025/month=07/day=08/device=123/


### Example 2: Query by device  
Structure:  
s3://bucket/device=123/year=2025/month=07/day=08/



---

## 🔗 Use Cases

- Creating SQL views on S3 data for Athena/Redshift
- Transforming raw JSON/CSV/Parquet data
- Scheduled ETL for data warehousing
- Auto-inference of schemas for unstructured logs

---

## ✅ Key Things to Remember

- Data stays in **S3** – Glue only extracts metadata/schema
- You can query unstructured S3 data **like SQL tables**
- Glue = the **“glue”** between data lakes and structured analytics

---

📘 Study Focus for MLE-A:
> Know how Glue integrates with S3, crawlers, ETL, and analytics services.

