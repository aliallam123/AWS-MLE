# SageMaker Domain - Exam Essentials (AWS MLE Associate)

## ✅ Key SageMaker Domain Concepts for the Exam

| Concept | What You Need to Know |
|--------|------------------------|
| **SageMaker Domain** | The root container for all SageMaker activity. You must create one before doing anything. |
| **Amazon EFS Volume** | Shared across the domain. Each user profile has a private directory carved from this shared EFS. |
| **User Profiles** | Represent individual users. Each profile owns personal apps (e.g. Studio). |
| **Shared Spaces** | Enable collaboration. Users can share data, notebooks, etc. via shared EFS space. |
| **Studio IDE** | Main interface for users; can be shared or individual. |
| **VPC Configuration** | Two VPCs by default: one managed by SageMaker (internet access), one your own (for private/encrypted traffic). You can opt for **VPC-only mode** to control all traffic. |
| **Security** | You define subnets and security groups for your VPC to isolate and protect resources. |

---

## 🎯 Why This Matters for the Exam

- Related to **Domain 3**: *Deployment and Orchestration of ML Workflows*.
- You may be tested on:
  - SageMaker Studio setup/configuration.
  - Access control through VPC and IAM.
  - Multi-user collaboration.
  - Storage and compute separation.
