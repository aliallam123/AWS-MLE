# Model Monitoring Best Practices – AWS MLE-A Notes

## Core Monitoring Tools
- 📊 **SageMaker Model Monitor** → detect drift, anomalies, data quality issues.  
- 🧾 **SageMaker Clarify** → bias detection, explainability, fairness.  
- 🗂️ **SageMaker Lineage Tracking** → track data, model, and pipeline history.  
- 📜 **Model Cards (Clarify)** → governance + documentation of model behavior.  
- 🔍 **CloudWatch** → system-level metrics/logs.  
- 🔄 **Autoscaling + Elastic Inference** → scale endpoint fleets automatically.  

---

## Best Practices

### Observability & Governance
- 🏗️ Synchronize infra/config → **CloudFormation + Model Monitor** (detect environment drift).  
- 🔐 Secure endpoints → IAM + VPC + GuardDuty/Macie for monitoring anomalous access.  
- 🗂️ Version control & rollback → **ECR, CodeCommit, SageMaker Pipelines/Projects**.  

### Drift & Explainability
- ⚖️ Detect bias/fairness changes → **Clarify**.  
- 📊 Visualize drift & metrics → **CloudWatch + OpenSearch**.  
- 🔍 Evaluate feature importance changes → Clarify + Model Monitor.  

### Retraining Strategy
- ⚡ Automate retraining → **Pipelines, Step Functions, Jenkins, SDK**.  
- 🧑‍⚖️ Add human-in-the-loop → **Amazon A2I** (quality review).  
- 🗂️ Review incoming data with **Data Wrangler** before retraining.  
- 🛑 Retrain **only when necessary** → define acceptable accuracy thresholds.  

### Cost & Efficiency
- 💸 Track usage & cost → **tagging + AWS Budgets + Cost Explorer**.  
- 📈 Monitor ROI/business value → **QuickSight dashboards**.  
- ⚙️ Right-size endpoint fleets → **CloudWatch + Autoscaling + Inference Recommender**.  
- 🗄️ For massive training → **Amazon FSx for Lustre** (higher throughput than S3).  
- ♻️ Define **material efficiency** = (Provisioned resources ÷ Business outcomes).  

---

## Sustainability & Practical Tips
- 🔄 Avoid unnecessary retraining (training = $$$ + energy).  
- ⚡ Use efficient storage/compute (FSx for Lustre, efficient silicon).  
- 🌱 Monitor provisioned vs. used capacity to reduce idle waste.  

---

## 🔑 Exam Tips
- **Model Monitor** = data drift + anomaly detection.  
- **Clarify** = bias + explainability.  
- **A2I** = human evaluation of results.  
- **Lineage Tracker** = governance + reproducibility.  
- **FSx for Lustre** = preferred storage for very large training jobs.  
- **Budgets/Cost Explorer** = track ML costs.  
- **Retrain only if accuracy/business goals require it** → not on a schedule.  

---
