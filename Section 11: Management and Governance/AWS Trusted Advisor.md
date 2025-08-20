# AWS Trusted Advisor – AWS MLE-A Notes

## Overview
- 🕴️ **Trusted Advisor** = High-level account assessment tool.  
- ✅ Gives recommendations across **6 categories**:  
  1. Cost Optimization 💸  
  2. Performance ⚡  
  3. Security 🔐  
  4. Fault Tolerance 🔄  
  5. Service Limits 📊  
  6. Operational Excellence 🏗️  

## Access Levels
- **Core checks (free)** → Limited set, mainly **security & service limits**.  
- **Full checks (paid)** → Requires **Business or Enterprise Support Plan**.  
- 📡 With Business/Enterprise, can also access via **Support API** (programmatic access).  

## Examples of Checks
- 🔐 Security: Public S3 buckets, unrestricted SG ports, public EBS/RDS snapshots, use of root account.  
- 💸 Cost Optimization: Idle resources, RI utilization (Business/Enterprise only).  
- 📊 Service Limits: Track resource quotas (e.g., DynamoDB capacity, Auto Scaling Groups).  

---

## 🔑 Exam Tips
- 🕴️ Trusted Advisor = **best practice recommendations** (account-wide).  
- 📦 **Budgets** = track + alert on cost.  
- 📊 **Cost Explorer** = analyze + forecast spend.  
- 🚫 Free plan = only **core checks** (mainly security & limits).  
- 💰 Full set = Business or Enterprise Support Plan required.  

---
