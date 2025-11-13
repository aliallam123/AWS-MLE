# ⚡ Training Trillion-Parameter Models on AWS – GitHub Revision Notes

## 🚀 Elastic Fabric Adapter (EFA)

- **What it is**: High-performance network adapter for SageMaker/EC2
- **Use case**: Speeds up communication between GPUs across instances
- **Requirements**:
  - Nvidia GPUs
  - **NCCL** (Nvidia Collective Communication Library)
  - **AWS NCCL plugin**
  - Env variable: `FI_PROVIDER=efa`
- **Benefits**:
  - On-par with on-prem HPC networking
  - Reduces communication latency in **multi-node** distributed training

---

## 🧠 MiCS (Minimize the Communication Scale)

- AWS architecture for **scaling beyond 1 trillion parameters**
- Combines:
  - EFA for high-speed networking
  - SageMaker **sharded data/model parallelism**
  - Massive EC2 instances like **P4d**
  - **FSx** for low-latency, high-throughput storage
- Enables building “GPT-20”-scale models (if you have the budget)

---

## 🏢 EC2 UltraClusters

- Underpin AWS’s **MiCS** strategy
- Example configuration:
  - 4,000+ Nvidia A100 GPUs
  - P4d instances with:
    - **400 Gbps networking**
    - **80 GB GPU memory**
  - High-speed **FSx storage**

---

## 💡 Exam Tips

- **EFA** = High-speed networking between GPUs (multi-node)
- **NCCL + EFA** = Required combo
- **MiCS** = AWS solution for trillion+ parameter models
- UltraClusters + EFA + sharded parallelism = Full stack for massive scale
