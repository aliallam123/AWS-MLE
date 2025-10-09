# Docker, ECS, EKS, and Container Management on AWS

## 🐳 What is Docker?

- Docker is a **containerization platform** used to package and deploy applications.
- Containers are **standardized, lightweight**, and **OS-independent**.
- Benefits:
  - Predictable, consistent app behavior
  - Easy deployment and maintenance
  - Compatible with all languages and OS

### 🔄 Use Cases
- Microservices architecture
- Lifting and shifting apps to the cloud
- Running containerized workloads

---

## 🧱 Docker Architecture vs Virtual Machines

### 🧰 Docker Architecture
- Runs containers on a host OS via the **Docker Daemon**
- Containers share the host’s kernel (lightweight, fast)
- Can share networking and some storage
- Less isolated than VMs but more resource-efficient

### 🖥️ Virtual Machine Architecture
- Runs via a **hypervisor**
- Each VM has its **own guest OS** (heavier)
- More isolation but uses more resources

---

## 📦 Docker Workflow

1. **Write a Dockerfile** – define container build instructions
2. **Build an image** – `docker build`
3. **Push to a repo**:
   - **Docker Hub** (public)
   - **Amazon ECR** (private/public AWS repo)
4. **Pull & Run** – Image becomes a container when executed

---

## ☁️ Docker on AWS – Key Services

| Service       | Purpose                                                      |
|---------------|--------------------------------------------------------------|
| **ECS**       | Elastic Container Service – AWS-native Docker orchestration  |
| **EKS**       | Elastic Kubernetes Service – Managed Kubernetes on AWS       |
| **Fargate**   | Serverless container compute engine for ECS/EKS              |
| **ECR**       | Elastic Container Registry – Stores Docker container images  |

### 🔁 ECS vs EKS
- **ECS**: Simplified, AWS-native container management
- **EKS**: Kubernetes-based, for more complex orchestration

---

## ✅ Exam Essentials

- Docker containers are more lightweight than VMs and share the host OS.
- **Docker Hub** = public repo; **Amazon ECR** = AWS-managed private/public repo.
- **Fargate** runs containers without managing servers; works with ECS & EKS.
- ECS is **AWS-native**; EKS is for those using **Kubernetes**.

## 🎯 Quick Tips

- “Run containers on AWS with full control” → Use **ECS**
- “Managed Kubernetes” → Use **EKS**
- “No servers, fully managed” → Use **Fargate**
- Store Docker images on **ECR** for private container repositories
