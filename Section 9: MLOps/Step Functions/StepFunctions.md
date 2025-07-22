# AWS Step Functions – Workflow Orchestration on AWS

## 🧠 What Is AWS Step Functions?

- **AWS Step Functions** is a **serverless orchestration service** to coordinate multiple AWS services into a single, automated workflow.
- Each workflow is called a **state machine**.

---

## ⚙️ Key Features

- **Visual workflow design**
- **Step-by-step orchestration** (e.g., Lambda → SageMaker → Batch)
- Built-in:
  - **Error handling**
  - **Retries**
  - **Wait/sleep states**
  - **Audit history**
- Supports **long-running workflows** (up to 1 year execution time)

---

## 🧱 Common Use Cases

- **ML pipelines**:
  - Data prep → Train → Tune → Batch inference (with SageMaker)
- **CI/CD pipelines**:
  - Build → Deploy → Validate → Notify
- **ETL coordination** (e.g., Glue → Transform → Save)
- **Batch job monitoring**
  - Monitor job → Notify on success/failure

---

## 🧪 Example Workflows

1. **ML Training Flow**:
   - Lambda (prep) → SageMaker training → SageMaker transform → Done

2. **Model Tuning Flow**:
   - Lambda → SageMaker HPO job → extract best model → batch inference

3. **Simple Job Monitoring**:
   - Submit AWS Batch job → wait → notify via SNS if failed

---

## ✅ Exam Essentials

- Defined in **Amazon States Language (ASL)** (JSON-based, no coding needed on exam)
- Visualized in the AWS Console
- Built-in **error handling, logging, and retries**
- Works with **Lambda, SageMaker, ECS, Batch, Glue, SQS, SNS**, and more
- Great for **data science workflows**, **MLOps**, and **automation pipelines**

## 🎯 Quick Tips

- “Multi-step process with retries & logic?” → **Step Functions**
- “Chaining SageMaker or Lambda steps?” → Use **Step Functions**
- “Visual workflow for orchestration?” → Think **Step Functions**
- Up to **1-year** execution time, **serverless**, **event-driven**
