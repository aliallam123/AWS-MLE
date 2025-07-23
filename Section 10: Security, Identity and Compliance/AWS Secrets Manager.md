# AWS Secrets Manager – Secure Secrets Storage & Rotation

## 🔐 What Is Secrets Manager?

**AWS Secrets Manager** is a fully managed service for securely storing, retrieving, and rotating **secrets** like database credentials, API keys, and tokens. It supports **automated secret rotation** using **Lambda functions**, integrates natively with services like **Amazon RDS**, and encrypts secrets using **AWS KMS**. Unlike SSM Parameter Store, Secrets Manager focuses on secret lifecycle management, rotation, and replication. You can also replicate secrets **across AWS regions** for high availability and disaster recovery scenarios.

## ✅ Exam Essentials

- Used for storing **secrets** (e.g., DB passwords, API keys)
- Supports **automated rotation** via Lambda
- **Integrated with RDS/Aurora** out of the box
- Secrets are **encrypted with KMS**
- Supports **multi-region replication** for DR and multi-region apps
- Not the same as **SSM Parameter Store** (less secure, no rotation)
