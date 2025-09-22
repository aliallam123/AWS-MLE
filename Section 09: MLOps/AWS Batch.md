# AWS Batch – Container-Based Batch Job Processing

## 🧠 What Is AWS Batch?

- Fully managed service for running **batch computing jobs** using **Docker containers**.
- **Serverless**: automatically provisions EC2 or Spot Instances based on job requirements.
- No need to manage compute clusters manually.

---

## ⚙️ Key Features

- **Dynamic compute provisioning**: EC2/Spot based on job volume.
- Supports **Docker images** for job definitions.
- Can be **scheduled** via **CloudWatch Events**.
- Can be **orchestrated** via **AWS Step Functions**.

---

## 🆚 AWS Batch vs AWS Glue

| Feature             | AWS Batch                             | AWS Glue                             |
|---------------------|----------------------------------------|--------------------------------------|
| Purpose             | General-purpose batch jobs             | ETL-only (Extract, Transform, Load)  |
| Runtime             | Any Docker image                       | Apache Spark (Python/Scala)          |
| Scheduling          | CloudWatch Events / Step Functions     | Integrated scheduling + triggers     |
| Use Case Example    | Cleanup scripts, simulations, reports  | Data wrangling, cataloging, ETL      |

---

## ✅ Exam Essentials

- Use **Batch** for **non-ETL jobs** that are batch-oriented (e.g. cleanup, simulations).
- Jobs must be **Dockerized** (you provide the container).
- Glue = **ETL**; Batch = **general-purpose containers**.
- Compute happens in your AWS account using EC2/Spot instances.

## 🎯 Quick Tips

- "Run Docker-based job on schedule" → **AWS Batch**
- "Spark ETL with cataloging" → **AWS Glue**
- "General-purpose batch job (non-ETL)" → **Batch**
- Uses EC2 compute managed **by Batch**, not you
