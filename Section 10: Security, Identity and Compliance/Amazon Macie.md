# AWS Macie – Data Classification for S3

## 🛡️ What Is Macie?

**Amazon Macie** is a fully managed data security and privacy service that uses **machine learning** and **pattern matching** to automatically **detect sensitive data** (like **PII**) in your **S3 buckets**. Once enabled, Macie scans specified S3 buckets and alerts you via **Amazon EventBridge** when it finds data matching patterns like names, email addresses, credit cards, etc. These alerts can then trigger **SNS**, **Lambda**, or other automated actions. It’s easy to enable and highly useful for data governance and compliance use cases.

## ✅ Exam Essentials

- Detects **PII** and other sensitive data in **S3**
- Integrates with **EventBridge** for alerts
- Can trigger downstream actions (SNS, Lambda)
- Focused **only on S3**
- Quick setup with one-click enablement
