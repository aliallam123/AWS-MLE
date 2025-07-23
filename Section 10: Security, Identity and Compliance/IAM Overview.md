# IAM for AWS Machine Learning Engineer – Associate (MLA-C01)

## 🔐 IAM Overview

- **IAM = Identity and Access Management**
- Manages **users**, **groups**, **roles**, and **permissions**
- IAM is **global** — no region selection

---

## 👤 Users, Groups, Roles

| Type     | Used For                                    |
|----------|---------------------------------------------|
| **User** | Individual login + permissions              |
| **Group**| Apply shared permissions to multiple users  |
| **Role** | AWS service-to-service access (e.g. SageMaker → S3) |

---

## 📜 Policies

- IAM policies are JSON documents that define:
  - **Effect**: Allow or Deny
  - **Action**: API actions (e.g. `s3:GetObject`)
  - **Resource**: ARNs (e.g. S3 buckets, Lambda functions)
- Use **managed policies** like:
  - `AmazonSageMakerFullAccess`
  - `AmazonSageMakerReadOnly`
- Use **inline policies** only when needed (not best practice at scale)

---

## 🧱 IAM Roles for SageMaker

- Needed for:
  - **Training jobs**
  - **Endpoints**
  - **Notebook execution**
- Example role: `AmazonSageMakerExecutionRole`
- Includes **trust policy** to allow SageMaker to assume the role

---

## 🔐 Password Policies

- Set minimum length, complexity
- Enforce password expiration
- Prevent reuse of previous passwords

---

## 🛡️ MFA (Multi-Factor Authentication)

- Strongly recommended on **root** and **IAM users**
- Types:
  - **Virtual MFA** (e.g. Authy, Google Authenticator)
  - **Hardware key** (e.g. YubiKey)
- Used to protect accounts with sensitive access

---

## 🧠 Security Tips for SageMaker

- SageMaker needs S3 access → use **IAM role + S3 policies**
- **Training in VPC?** → Create **S3 VPC endpoint**
- If **no internet access**, use:
  - **VPC endpoint (Privatelink)**
  - or **NAT Gateway** for outbound traffic

---

## 📊 Monitoring & Auditing

| Service       | Purpose                     |
|---------------|-----------------------------|
| **CloudTrail**| Auditing → logs API actions |
| **CloudWatch**| Monitoring/logging → metrics, alarms |

---

## ✅ Exam Takeaways

- Use IAM roles to give SageMaker scoped access to S3/KMS
- IAM policies must specify: Effect, Action, Resource
- Always follow **least privilege**
- Know difference between **CloudTrail** (audit) and **CloudWatch** (metrics)
- Enable **MFA** on root/admin accounts
- Use **IAM policies** to control access to expensive actions (e.g. tuning jobs)

---

## 🎯 Quick Tips

- “Give SageMaker access to encrypted S3 data?” → IAM role + KMS + VPC endpoint
- “Log every API action across AWS?” → Use **CloudTrail**
- “Control who can launch tuning jobs?” → Use **IAM policies**
- “Avoid root usage, enable MFA” → ✅ Always secure root access

