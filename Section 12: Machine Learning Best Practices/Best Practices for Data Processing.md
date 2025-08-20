# Data Processing Best Practices – AWS MLE-A Notes

## Stages
1. **Data Collection**
   - Gather data → labeling (manual or automated with **Ground Truth**).
   - Ingest via batch/stream into **S3** or data lake.
   - Aggregate/partition for scalability (by time, feature, etc.).

2. **Data Preparation**
   - Clean data: handle missing values, outliers.
   - Partition data for efficient access.
   - Balance/unbias data (avoid skewed training sets).
   - Augment with external/new data if needed.

3. **Feature Engineering**
   - Select key features, discard irrelevant.
   - Transform: normalization, one-hot encoding.
   - Create new derived features (e.g., square root, extracted fields).
   - Enable feature reuse via **SageMaker Feature Store**.

---

## Best Practices with AWS Services
- 📊 **Profile & improve data quality**  
  - Tools: **Data Wrangler, Glue, Athena, Redshift, QuickSight**.  

- 🗂️ **Tracking & versioning**  
  - **SageMaker Experiments** (track datasets/models).  
  - **Model Registry** (link datasets to model versions).  
  - Store notebooks in **Git**.  

- 🔐 **Security**  
  - Enforce **least privilege IAM**.  
  - Use **KMS**, **Secrets Manager**, **VPC + PrivateLink**.  
  - Protect privacy → **Amazon Macie** (PII detection).  

- 🧾 **Lineage & Cataloging**  
  - **SageMaker ML Lineage Tracker** → data + pipeline history.  
  - **AWS Glue Catalog** → schema for un/semi-structured data.  

- ⚙️ **Pipelines & automation**  
  - **SageMaker Pipelines** → define processing workflows.  
  - Automate data changes & lifecycle management.  

- 🧑‍🏫 **Data Labeling**  
  - Use **Amazon Ground Truth** for managed labeling.  

- 🧑‍💻 **Data Wrangling**  
  - Interactive transformations → **SageMaker Data Wrangler**.  

- 🔄 **Managed Processing**  
  - Use **SageMaker Processing** for scalable compute.  

---

## Sustainability & Cost Control
- 💤 Minimize idle resources → prefer managed services.  
- 📦 Implement lifecycle policies (delete/archive unused data).  
- ❄️ Use cheaper storage tiers (e.g., **S3 Glacier**).  
- 🌱 Adopt sustainable regions/storage where possible.  

---

## 🔑 Exam Tips
- 🧑‍🏫 **Ground Truth** = managed data labeling.  
- 📊 **Data Wrangler** = profiling + transformation.  
- 🗂️ **Feature Store** = reusable features across models.  
- 🔐 **Macie** = PII detection, **Glue Catalog** = schema mgmt.  
- 🧾 **Lineage Tracker** = trace data usage + model input history.  
- 💸 Sustainability = use Glacier, lifecycle policies, managed services.  

---
