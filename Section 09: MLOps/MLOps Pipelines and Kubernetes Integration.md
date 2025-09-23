# SageMaker MLOps – Projects, Pipelines, and Kubernetes Integration

## 🧠 What Is MLOps?

- MLOps = Managing the end-to-end ML lifecycle:
  - Data prep, model training, deployment, monitoring, updates.
- Focus: Automation, reproducibility, scalability.

---

## 🔁 1. SageMaker Projects + Pipelines

- **SageMaker Projects**: Native MLOps platform within SageMaker Studio.
- **SageMaker Pipelines**: Define sequential steps like:
  - Data processing → Training → Evaluation → Model registration.
- Integrates with:
  - **CodeCommit / GitHub**
  - **CodePipeline, CodeBuild, EventBridge**
  - **CloudFormation (for endpoint deployment)**
- Example Flow:
  - Code commit → EventBridge → CodePipeline → CodeBuild → SageMaker Pipeline → Model Registry → Deployment to staging/production

---

## ☸️ 2. SageMaker Operators for Kubernetes

- Kubernetes-native wrapper to trigger SageMaker jobs from `kubectl`.
- Run on **Amazon EKS**.
- Supports:
  - Training
  - Tuning
  - Processing
  - Inference
- Useful for **hybrid setups** or gradual migration from Kubernetes to SageMaker.

---

## ⚙️ 3. SageMaker Components for Kubeflow Pipelines

- Integrates SageMaker into **Kubeflow** MLOps pipelines.
- Components for:
  - Data processing
  - Training
  - Tuning
  - Deployment
- Good for teams already using **Kubeflow + Kubernetes**.

---

## ✅ Exam Essentials

- “Starting from scratch with SageMaker”? → Use **SageMaker Projects + Pipelines**
- “Already using Kubernetes”? → Use **SageMaker Operators**
- “Using Kubeflow Pipelines”? → Use **SageMaker Components**
- Projects = Full CI/CD; Pipelines = ML workflow steps

---

## 🎯 Quick Tips

- CI/CD keywords (e.g., Git, CodePipeline, EventBridge) → **SageMaker Projects**
- `kubectl` + training jobs = **Operators for Kubernetes**
- “Kubeflow integration” = **SageMaker Components for Kubeflow**
- “Model registry, monitoring, retraining” → **Pipelines**
