# AWS CloudTrail – AWS MLE-A Notes

## Overview
- 📜 **CloudTrail** = Governance, compliance, audit trail for AWS accounts.  
- 🔧 Logs all **API calls** (Console, CLI, SDK, AWS services).  
- ✅ Enabled by default.  
- 📊 Default retention = **90 days** (longer storage = send to S3, analyze with Athena).  

## Event Types
1. **Management Events**  
   - Control-plane actions (e.g., CreateSubnet, AttachRolePolicy).  
   - Separated into:  
     - **Read events** (e.g., ListUsers).  
     - **Write events** (e.g., DeleteTable).  
   - Logged by default.  

2. **Data Events**  
   - High-volume, resource-level activity.  
   - Examples:  
     - **S3 object-level** → GetObject, PutObject, DeleteObject.  
     - **Lambda execution** → Invoke function.  
   - ❌ Not logged by default (must be enabled).  

3. **Insights Events**  
   - 🔎 Detect **anomalies/unusual activity** in management events.  
   - Examples: abnormal IAM activity, service limit spikes.  
   - Requires **explicit enable + extra cost**.  
   - Can send anomalies to **EventBridge** for automated responses.  

## Retention & Storage
- Default: **90 days in CloudTrail**.  
- Long-term: Store in **S3**.  
- 🔍 Analyze with **Athena** for historical queries.  

---

## 🔑 Exam Tips
- 🎥 CloudTrail = **“Who did what, when, and from where?”**.  
- 🛠️ **Management Events** = control-plane (default logged).  
- 📦 **Data Events** = resource-level (S3 objects, Lambda invocations).  
- 🚨 **Insights** = anomaly detection for management events.  
- ⏳ For >90 days retention → **export to S3**.  
- 🔔 Integrate with **EventBridge** or **CloudWatch Logs** for alerting/automation.  

---
