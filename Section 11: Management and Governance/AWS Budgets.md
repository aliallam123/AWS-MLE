# AWS Budgets – AWS MLE-A Notes

## Overview
- 💰 **AWS Budgets** = Track and control costs, usage, and discounts.  
- 🔔 Create alarms if **actual** or **forecasted** charges exceed thresholds.  
- 🌍 Granular filters (by service, account, tag, purchase options, etc.).  
- 📈 More flexible than CloudWatch billing alarms.  

## Types of Budgets
1. **Usage Budgets** → Track usage (e.g., hours of EC2).  
2. **Cost Budgets** → Track actual or forecasted spend.  
3. **RI (Reserved Instance) Budgets** → Track RI utilization & coverage (EC2, RDS, ElastiCache, Redshift).  
4. **Savings Plan Budgets** → Track utilization & coverage.  

## Notifications
- 📧 Up to **5 notifications per budget** (via SNS/email).  
- ✅ First **2 budgets free**, then $0.02 per day per budget.  

---

## 🔑 Exam Tips
- 🛠️ Use **AWS Budgets** (not CloudWatch) for **forecasted spend alerts**.  
- 📊 Use RI & Savings Plan budgets to track **utilization and coverage**.  
- 🔔 Budgets are **per-account** but can filter by tags/services.  
- 💸 Cheap to run → very common cost-control tool.  

---
