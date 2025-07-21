# SageMaker Auto Scaling and Availability Zones

## ⚙️ Automatic Scaling

- Automatically adjusts number of **inference instances** based on metrics.
- Configure:
  - **Target metric** (e.g., invocations per instance, latency)
  - **Min/Max capacity**
  - **Cooldown periods**
- Works at the **production variant level**.
- Integrated with **CloudWatch** for monitoring.

## 🧪 Best Practices

- **Load test scaling policies** in staging before deploying to production.
- Poor configuration may lead to under-provisioning or cost spikes.

## 🌍 Availability Zones (AZs)

- SageMaker spreads endpoints across **multiple AZs** for resiliency.
- Requires:
  - **2+ endpoint instances**
  - **Custom VPC** with **at least 2 subnets** in **different AZs**

## ✅ Exam Essentials

- Auto scaling uses CloudWatch + scaling policy configs.
- Scaling is done **per production variant**.
- Multi-AZ only works with **multiple instances** + properly zoned VPC subnets.

## 🎯 Quick Tips

- Mention of “cooldown”, “metric-based scaling” → Think **Auto Scaling**
- Want AZ-level high availability? → Use **2+ instances + multi-AZ subnets**
- Don’t skip **load testing** your scaling config before go-live.
