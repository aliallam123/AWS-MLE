# AWS Config – AWS MLE-A Notes

## Overview
- 🕵️ **Config** = Auditing + compliance monitoring for AWS resources.  
- ✅ Records **resource configurations over time**.  
- 📜 Can evaluate compliance against **rules** (AWS-managed or custom).  
- 🌍 Per-region service (can aggregate across accounts/regions).  
- 🔗 Works well with **CloudTrail** (see config changes + API calls together).  

## Rules
- **AWS Managed Rules** → ~75 prebuilt checks (e.g., no public S3 buckets, no 0.0.0.0/0 in SG).  
- **Custom Rules** → defined with **Lambda functions**.  
- Rules can trigger:  
  - On **configuration change**.  
  - On **periodic schedule**.  
- ⚠️ **Important**: Config **does NOT block** non-compliant actions (not a firewall/deny mechanism).  

## Remediation
- 🚑 Auto-remediation with **SSM Automation Documents** (AWS-managed or custom).  
- Examples:  
  - Disable IAM keys older than 90 days.  
  - Remove unrestricted SSH from SGs.  
- Can retry remediation multiple times.  
- Can also invoke **Lambda** for custom fixes.  

## Notifications
- 🔔 Non-compliance events → **EventBridge** or **SNS**.  
- Supports **SNS message filtering** for targeted notifications (e.g., only send SG-related issues to security team).  

## Cost
- 💰 $0.003 per configuration item recorded (per region).  
- 💰 $0.001 per rule evaluation (per region).  

## Use Cases
- ✅ Track resource changes over time.  
- ✅ Audit security posture (e.g., SGs, S3 buckets).  
- ✅ Trigger remediation workflows.  
- ✅ Centralize compliance view across multiple accounts/regions.  

---

## 🔑 Exam Tips
- 🕵️ Config = **compliance + history of configurations** (not API calls).  
- 🚫 Doesn’t block non-compliant resources, but can **auto-remediate** with SSM.  
- 🔗 Combine with **CloudTrail** for full audit picture.  
- 🌍 Must be enabled in each region (can aggregate centrally).  
- 📧 Use **SNS/EventBridge** for compliance alerts.  

---
