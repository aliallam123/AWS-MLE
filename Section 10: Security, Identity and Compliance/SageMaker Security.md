# SageMaker Security Best Practices & Exam Tips (MLA-C01)

This file summarizes all essential security practices related to Amazon SageMaker — a core topic in **Domain 4: ML Solution Monitoring, Maintenance, and Security** of the AWS Certified Machine Learning Engineer – Associate exam.

---

## 🔐 1. IAM Roles and Permissions

### ✅ SageMaker Execution Role
- Every SageMaker job (training, processing, hosting) needs an **IAM execution role**.
- The role must have access to:
  - **S3 buckets** for data input/output
  - **ECR** for Docker containers (if using custom containers)
  - **CloudWatch Logs** for monitoring
- Use **AmazonSageMakerFullAccess** *only for testing*. For production, follow **least privilege**.

### ✅ Role Delegation
- You can use **AssumeRole** to allow SageMaker to use other services (e.g., Lambda invoking SageMaker).
- Use **trust policies** carefully to avoid privilege escalation.

---

## 🌐 2. VPC Network Isolation

### ✅ VPC Support for SageMaker
- SageMaker supports **VPC endpoints** to **isolate** training/inference jobs.
- Use **PrivateLink** to access S3 and other AWS services **without going over the public internet**.
- Make sure to:
  - Set up **security groups** to limit access.
  - Deploy endpoints into **private subnets** for added security.

### ✅ Secure Hosting
- Model endpoints can be deployed into a VPC with:
  - **Inbound/Outbound rules**
  - **Security groups** controlling access
  - Prevents public access by default

---

## 🔒 3. Encryption at Rest and In Transit

### ✅ At Rest
- All data stored by SageMaker (model artifacts, training data, logs) is encrypted using:
  - **AWS-managed KMS keys** by default
  - Optionally: your own **Customer Managed Key (CMK)** via KMS

### ✅ In Transit
- SageMaker encrypts data in transit using **TLS (Transport Layer Security)**.
- Applies to:
  - API calls
  - Communication with S3, EFS, etc.

---

## 🧠 4. SageMaker Role Manager

### What it Does:
- Simplifies the creation of IAM roles tailored to specific **SageMaker personas**:
  - **Data Scientist**
  - **ML Engineer**
  - **Model Reviewer**

### Why it Matters:
- Helps enforce **least privilege** and avoid overly broad access.
- Prevents accidental access to training data, model registry, etc.

---

## 📜 5. Logging, Auditing & Monitoring

### ✅ CloudTrail
- Tracks:
  - SageMaker job starts/stops
  - Endpoint creation/deletion
  - API calls for training, inference, etc.

### ✅ CloudWatch
- Collects logs and metrics from:
  - Training jobs
  - Processing jobs
  - Endpoints (e.g., latency, invocation count)

Use alarms to **detect anomalies**, **cost spikes**, or **model drift**.

---

## ✅ Exam Tips

💡 **Expect Questions On:**
- Choosing the right role and permissions for SageMaker jobs
- Whether network isolation is required in a specific scenario (→ choose VPC config)
- How to use KMS for encryption (e.g., rotating keys, CMK vs AWS-managed)
- Protecting endpoint access using security groups and VPC
- Detecting unauthorized access or configuration changes using CloudTrail

🧠 **Remember**:
- Security best practice = **Least privilege + Encryption + Network Isolation**
- VPC + KMS + IAM + CloudTrail = 🔐 secure ML workflow

---

## 🔗 Related Services to Know

- [AWS KMS](https://docs.aws.amazon.com/kms/latest/developerguide/overview.html)
- [IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
- [CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)
- [CloudWatch](https://docs.aws.amazon.com/cloudwatch/)
- [SageMaker Security Best Practices](https://docs.aws.amazon.com/sagemaker/latest/dg/security.html)

---

