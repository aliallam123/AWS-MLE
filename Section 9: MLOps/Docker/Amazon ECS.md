# Amazon ECS: Deep Dive Overview

## 🚀 What Is Amazon ECS?

- **ECS** = Elastic Container Service – AWS-managed Docker orchestration.
- You launch **ECS Tasks** into **ECS Clusters** using:
  - **EC2 Launch Type**
  - **Fargate Launch Type**

---

## 🖥️ EC2 Launch Type

- ECS Cluster runs on **user-managed EC2 instances**.
- You must:
  - Provision EC2 instances
  - Install ECS Agent on each
  - Manage capacity and scaling
- Containers are placed on EC2 instances by ECS scheduler.

---

## ☁️ Fargate Launch Type (Serverless)

- **No infrastructure management** – AWS provisions compute automatically.
- You define **task definition**, including CPU & memory.
- Fully managed, scalable, **serverless** container execution.
- **Recommended in the exam** due to simplicity.

---

## 🔐 IAM Roles in ECS

| Role Type            | Applies To     | Purpose                                               |
|----------------------|----------------|--------------------------------------------------------|
| **EC2 Instance Profile** | EC2 Launch Type | Allows ECS Agent to interact with AWS services (ECR, CloudWatch, Secrets Manager) |
| **ECS Task Role**        | Both launch types | Grants specific permissions to ECS tasks (e.g., Task A accesses S3, Task B accesses DynamoDB) |

- **Defined inside ECS task definition**.

---

## 🌐 Load Balancer Integration

- Use **Application Load Balancer (ALB)** for most ECS services (including Fargate).
- **Network Load Balancer (NLB)** for:
  - High performance/throughput
  - Use with **AWS PrivateLink**
- **Classic Load Balancer**:
  - Legacy; not supported with Fargate.
  - Not recommended.

---

## 🗄️ Persistent Storage with ECS

- Use **Amazon EFS** (Elastic File System) for shared data volumes.
- Works with both **EC2 and Fargate** launch types.
- Use cases:
  - Persistent, **multi-AZ** shared storage
  - Stateless containers needing shared state or communication

### ✅ Benefits of EFS:
- Fully **serverless**, pay-as-you-go
- Mounted directly onto ECS tasks
- Supports parallel access from multiple AZs

---

## ✅ Exam Essentials

- **Fargate** = Serverless, recommended, no EC2 management.
- **EFS** = Persistent storage for multi-AZ containers.
- **ALB** = Default choice for exposing ECS services.
- **IAM Roles**:
  - **Instance Profile** = EC2 agent-level
  - **Task Role** = Task-specific AWS service access
- ECS can be used with **EFS for shared state** and **ALB for load balancing**.

## 🎯 Quick Tips

- If “no server management” → Use **Fargate**
- If “share data between tasks” → Use **EFS**
- If “load balance container tasks” → Use **ALB**
- ECS task needs to call AWS service? → Assign a **Task Role**
