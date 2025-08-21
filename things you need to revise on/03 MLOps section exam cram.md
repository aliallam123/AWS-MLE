# 🚀 Last-Minute Cram – Deployment & Orchestration (MLE-A)

## CodePipeline
CI/CD for apps.  
Exam keyword: “build, test, deploy app”, integrates with SageMaker for model deployment.  
❌ Not for retraining on new data → use SageMaker Pipelines + EventBridge.  

---

## Docker / Docker Containers
Package ML code into containers.  
Exam keyword: BYOC (Bring Your Own Container) in SageMaker.  
Stored in ECR → deploy to SageMaker / ECS / EKS.  

---

## Amazon ECS / EKS
ECS = container orchestration (AWS managed).  
EKS = Kubernetes on AWS (more control).  
Exam keyword: deploy ML models at scale outside SageMaker.  

---

## ECR (Elastic Container Registry)
Stores Docker images.  
Exam keyword: registry for custom ML containers.  

---

## SageMaker Model Monitor
Monitors deployed models → detects drift, bias, data quality issues.  
Exam keyword: “monitor production model, detect drift” → Model Monitor.  
Sends alerts via CloudWatch.  

---

## Step Functions
General orchestrator (state machines).  
Exam keyword: “complex workflows across multiple AWS services”.  
If only ML workflow → SageMaker Pipelines.  

---

## AWS Batch
Run large batch compute jobs.  
Exam keyword: scheduled batch ML inference.  
Compare with SageMaker Batch Transform (purpose-built).  

---

## AWS CDK (Cloud Development Kit)
Define infra in code (IaC).  
Exam keyword: IaC for ML infra.  
Alternatives: CloudFormation.  

---

## AWS CloudFormation
Declarative IaC.  
Exam keyword: provision SageMaker endpoints, pipelines reproducibly.  

---

## AWS Lake Formation
Build/secure data lakes.  
Exam keyword: set up S3 data lake for ML with fine-grained permissions.  

---

## Deployment Guardrails
Safe deployment strategies: blue/green, canary, shadow testing.  
Exam keyword: safe rollback, test new models gradually.  

---

## EventBridge
Event bus (serverless).  
Exam keyword: “S3 new data → trigger SageMaker Pipeline”.  
Always the answer for event-driven ML retraining.  

---

## Inference Deployment Options
- Real-Time → steady traffic, immediate.  
- Serverless → fluctuating traffic, immediate.  
- Async → fluctuating, not immediate.  
- Batch Transform → offline bulk.  
Exam keyword: map scenario → endpoint.  

---

## Inference Pipelines
Chain multiple models/preprocessing steps.  
Exam keyword: “preprocess + predict in one endpoint”.  

---

## MLOps Pipelines + Kubernetes Integration
MLOps = automate retraining, deployment, monitoring.  
EKS/ECS → run ML workflows with containers.  
Exam keyword: CI/CD for ML.  

---

## MWAA (Managed Workflows for Apache Airflow)
Managed Airflow for orchestration.  
Exam keyword: custom ML pipelines beyond SageMaker Pipelines.  

---

## Neo and Edge Cases
SageMaker Neo → optimize models for edge devices (IoT, mobile, embedded).  
Exam keyword: deploy optimized ML at the edge.  

---

## SageMaker Auto Scaling + AZ
Endpoints can auto scale by invocations, latency, CPU utilization.  
Exam keyword: handle variable load, multi-AZ for HA.  

---

## SageMaker Resource Management
Manage compute, storage, networking for ML jobs.  
Exam keyword: pick right instance family (p3/p4/trn1/inf1/c/m/r).  

---

## Serverless Inference & Inference Recommender
Serverless Inference → real-time + fluctuating traffic.  
Inference Recommender → suggests best instance type for inference (perf vs cost).  
Exam keyword: optimize inference infra automatically.  

---

# ⚡ Ultra-Shortcut
- New data → retrain → EventBridge + SageMaker Pipelines.  
- Monitor drift → SageMaker Model Monitor.  
- Inference choice → map keywords (real-time, batch, async, serverless).  
- Safe deploy → Deployment Guardrails.  
- Containers → Docker + ECR + ECS/EKS.  
- IaC → CDK / CloudFormation.  
- Edge ML → SageMaker Neo.  
- Auto scaling inference → SageMaker Auto Scaling.  
