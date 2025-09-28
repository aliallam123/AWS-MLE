# Amazon MWAA – Managed Workflows for Apache Airflow

## 🧠 What Is Amazon MWAA?

- **Amazon MWAA** = Managed Workflows for Apache Airflow
- Provides a **fully managed Apache Airflow environment** for orchestrating data workflows using **Python-based DAGs**
- Useful for **ETL pipelines**, **ML model prep**, and other **custom batch workflows**

---

## 🧱 Key Concepts

- **Apache Airflow**: Open-source workflow tool that uses **DAGs** (Directed Acyclic Graphs) written in Python
- **MWAA** handles:
  - Environment setup
  - Auto-scaling of workers
  - Security and access control
  - VPC networking and endpoints

---

## 🔧 How It Works

- DAGs are written in Python and uploaded to **Amazon S3**
- MWAA reads DAGs and executes them as workflows
- Workflows can trigger:
  - **S3**
  - **Lambda**
  - **Glue**
  - **SageMaker**
  - **Athena**, **Redshift**, **Batch**, and more

---

## 🛠️ Features

- **Managed environment**: No need to install or configure Airflow yourself
- **Scalable workers**: Based on AWS Fargate containers
- **Web UI**: Airflow dashboard accessible via public or private endpoints
- **Integrates with IAM**, **Secrets Manager**, and VPC endpoints
- **Custom plugins & Python packages** supported via ZIP file uploads

---

## 🧪 Example Use Cases

- Complex ETL pipelines with conditional logic
- ML data preprocessing pipelines
- Coordinating tasks across AWS services in a Python-defined workflow

---

## ✅ Exam Essentials

- **MWAA = Apache Airflow on AWS**
- Workflows are defined as **Python DAGs**
- Integrates with many AWS services (S3, Lambda, Glue, SageMaker, etc.)
- **Alternative to Step Functions** for users familiar with Airflow or needing custom DAG control
- Fully managed, runs within a **VPC**, uses **Fargate**

## 🎯 Quick Tips

- “Python-based DAG orchestration?” → **MWAA**
- “Need to migrate existing Airflow DAGs to AWS?” → **Use MWAA**
- “Drag-and-drop?” → ❌ No, must write Python DAGs manually
- “Alternative to Step Functions for ETL/ML?” → ✅ **MWAA**
