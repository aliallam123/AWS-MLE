# AWS CloudFormation – Infrastructure as Code (IaC)

## 🧠 What Is CloudFormation?

- **CloudFormation** is a service for deploying AWS infrastructure using **code templates** (YAML or JSON).
- It automatically provisions, configures, and manages AWS resources in the correct order.

---

## 🧱 Key Features

- **Declarative syntax**: Describe *what* you want, not *how* to do it.
- **Repeatable deployments**: Launch the same infra across multiple regions/accounts/environments.
- **Template-driven**: Can include EC2, S3, VPC, Load Balancers, IAM, RDS, and more.
- **Auto resource ordering**: CloudFormation handles dependencies and order of creation.
- **Cost-saving automation**: Delete stacks at night, recreate in the morning.
- **Resource tagging & cost estimation**: Resources are grouped and trackable by stack.

---

## 📦 Benefits

- Infrastructure is **version-controlled** and **reviewable** like application code.
- Supports **custom resources** for unsupported AWS features.
- **Visualisation** via **Infrastructure Composer** shows relationships between resources.
- Compatible with **CI/CD pipelines** and **multi-account setups**.

---

## ✅ Exam Essentials

- Used for **infrastructure as code** across **regions**, **environments**, and **accounts**.
- Helps reduce manual setup, improves reliability, and aligns with DevOps practices.
- CloudFormation supports **almost all AWS resources**; others can be added with **custom resources**.
- Great for **repeatable**, **auditable**, and **automated** infrastructure deployment.

## 🎯 Quick Tips

- “Define infrastructure using templates” → **CloudFormation**
- “Automate resource creation/deletion” → **CloudFormation stack**
- “Architecture repeatable across regions” → Use **CloudFormation**
- YAML/JSON templates = declarative = no need to script ordering
