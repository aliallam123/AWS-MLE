# 🧠 Amazon Athena – Full Breakdown (MLE-A Exam)

## 🔍 What is Athena?

- Serverless, interactive **SQL query service** for data stored in **Amazon S3**
- No need to move or load data into databases
- Queries unstructured, semi-structured, or structured data
- Built on **Presto** (but evolved into its own service)

---

## ⚙️ How It Works

- Reads data **directly from S3**
- Uses **AWS Glue Data Catalog** to get table schemas
- Pay-per-query model: **$5 per TB scanned**
- Supports **partitioning** and **columnar formats** for performance and cost savings

---

## 📦 Supported Data Formats

| Format   | Human-Readable | Columnar | Splittable |
|----------|----------------|----------|------------|
| CSV/TSV  | ✅              | ❌       | ❌         |
| JSON     | ✅              | ❌       | ❌         |
| Avro     | ❌              | ❌       | ✅         |
| Parquet  | ❌              | ✅       | ✅         |
| ORC      | ❌              | ✅       | ✅         |

📌 Use **Parquet or ORC** for better performance and lower cost.

---

## 🧪 Common Use Cases

- Querying:
  - **Web logs, CloudTrail logs, VPC logs, ELB logs** stored in S3
- **Exploratory Data Analysis (EDA)**
- **Pre-Redshift staging**: Analyze before loading to warehouse
- Lightweight alternative to Elasticsearch for log querying

---

## 🔗 Integrations

- **Glue Data Catalog**: Table and partition schema management
- **Amazon QuickSight**: Visualize Athena query results
- **Jupyter, Zeppelin, RStudio**: JDBC/ODBC-compatible

---

## 🔐 Security

- **Access Control**:
  - IAM policies (e.g., `AmazonAthenaFullAccess`)
  - S3 bucket policies
- **Encryption Options**:
  - SSE-S3 (server-side encryption with S3 managed keys)
  - SSE-KMS (server-side with KMS)
  - CSE-KMS (client-side encryption with KMS)
- **Cross-account S3 access** via bucket policies
- **TLS** used for in-transit security

---

## 👥 Workgroups

- Group users, teams, or apps
- Set **query limits**, **encryption**, and **IAM policies**
- Track **costs by group** and isolate **query history**
- Integrated with **CloudWatch**, **SNS**, and **IAM**

---

## 💸 Cost Model

- **$5 per TB scanned**
- ✅ You pay for:
  - Successful queries
  - Cancelled queries
- ❌ You do **not** pay for:
  - Failed queries
  - DDL operations (`CREATE`, `DROP`, `ALTER`)
- **Partitioning** and **columnar formats** reduce scan size → save money

---

## 🚫 Anti-Patterns (What NOT to use Athena for)

- ❌ ETL jobs → use **AWS Glue** or **Apache Spark**
- ❌ Rich visualisation → use **Amazon QuickSight**
- Athena is best for **ad hoc queries** and **data exploration**

---

## ✅ MLE-A Exam Tips

- Know Athena is **serverless** and **SQL-based**
- Understand integration with **Glue Crawlers & Data Catalog**
- Remember **ORC/Parquet** = best formats for speed/cost
- Partitioned S3 layout = better query efficiency
- Use **Workgroups** for isolation, limits, IAM, and billing
- Understand **encryption options** and **access control**
- Expect **log analysis** and **cost-optimisation** scenarios
