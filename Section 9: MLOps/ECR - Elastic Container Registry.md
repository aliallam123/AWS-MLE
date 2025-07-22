# Amazon ECR – Elastic Container Registry

## 🐳 What Is Amazon ECR?

- **Amazon ECR (Elastic Container Registry)** is a managed Docker image repository in AWS.
- Used to **store, manage, version, and scan** Docker images for deployment.
- Can be used with:
  - **Amazon ECS**
  - **Amazon EKS**
  - **AWS Lambda** (for container-based functions)

---

## 🔐 Types of Repositories

- **Private Repositories**:
  - Scoped to your AWS account or shared across accounts
- **Public Repositories**:
  - Images can be accessed publicly via the **ECR Public Gallery**

---

## ⚙️ Key Features

| Feature                     | Description                                       |
|-----------------------------|---------------------------------------------------|
| **IAM Integration**         | Access to ECR is controlled via IAM roles/policies |
| **S3-backed Storage**       | Images stored behind the scenes in Amazon S3     |
| **Lifecycle Policies**      | Auto-expire old images to save storage costs     |
| **Image Tagging & Versioning** | Organise and manage image versions            |
| **Vulnerability Scanning**  | Detect security issues in container images       |

---

## 🔁 ECS Integration

- ECS tasks (Fargate or EC2) **pull images from ECR**.
- Requires appropriate **IAM permissions**:
  - EC2 instance role or ECS task role must allow `ecr:GetAuthorizationToken`, `ecr:BatchGetImage`, etc.

---

## ✅ Exam Essentials

- Store Docker images on **ECR**, not Docker Hub, in real AWS production setups.
- For image pulling errors, **check IAM role permissions**.
- ECR integrates seamlessly with **ECS** and other container services.
- ECR is **highly likely to appear** in ECS/Fargate deployment scenarios.

## 🎯 Quick Tips

- "Where to store/pull Docker images on AWS?" → **Amazon ECR**
- Mention of image scanning, tagging, or lifecycle rules → Also **ECR**
- ECS pulls images from ECR, using IAM roles for access
