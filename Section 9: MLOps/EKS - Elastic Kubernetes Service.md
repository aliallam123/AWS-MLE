# Amazon EKS – Elastic Kubernetes Service

## ☸️ What Is Amazon EKS?

- **EKS** = Managed **Kubernetes** service on AWS.
- Kubernetes is **open-source**, cloud-agnostic, and widely adopted.
- Used for **automating deployment, scaling, and managing containerized apps**.
- Alternative to Amazon ECS, with a different API and architecture.

---

## 🧱 EKS Launch Modes

| Mode               | Description                                     |
|--------------------|-------------------------------------------------|
| **EC2 Launch**      | Use EC2 as worker nodes (self/managed options) |
| **Fargate Launch**  | Serverless containers – no EC2 management      |

---

## 🔧 Node Management Options

1. **Managed Node Groups**:
   - AWS provisions and manages EC2 nodes.
   - Nodes are in an **Auto Scaling Group**.
   - Supports On-Demand & Spot instances.

2. **Self-managed Nodes**:
   - You provision and register EC2 nodes manually.
   - Can use prebuilt or custom AMIs.

3. **Fargate**:
   - No nodes to manage – fully serverless container deployment.
   - Simplifies scaling and infrastructure management.

---

## 📦 Storage in EKS (via CSI)

- **EBS** – Block storage for EC2-based pods.
- **EFS** – Only option supported with Fargate.
- **FSx for Lustre/NetApp** – Supported for high-performance needs.
