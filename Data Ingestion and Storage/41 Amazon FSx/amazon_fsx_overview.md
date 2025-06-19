# Amazon FSx - Overview and Summary for AWS MLE Associate Exam

## 🧠 What is Amazon FSx?
Amazon FSx is a **fully managed file storage service** that lets you launch and run file systems built on popular file system technologies. It provides **high performance, scalable, and cost-efficient file storage** in the cloud.

## 🪵 FSx Offers 4 File System Types

| FSx Type             | Based On              | Best For |
|----------------------|------------------------|----------|
| FSx for Lustre       | Lustre                 | ML/AI, HPC, data lakes |
| FSx for Windows File Server | Windows Server NTFS | Windows-based apps |
| FSx for NetApp ONTAP | NetApp ONTAP           | Enterprise apps needing snapshots, clones, etc. |
| FSx for OpenZFS      | OpenZFS                | Linux/Unix workloads |

---

## ✍️ What You Need to Know for the Exam:
- FSx is **in-scope** for the exam as a core data storage and processing option.
- Know **when to use FSx vs EFS vs EBS vs S3**.
- FSx for Lustre integrates with **S3** for fast data access (great for SageMaker training).
- FSx file systems can be used as **training data sources** for Amazon SageMaker.
- Supports **high throughput**, **low-latency**, and **POSIX compliance** (depending on FSx type).
- Great for scenarios where you need **shared, performant, or specialised file systems**.

---

## 🚀 FSx Use Cases in ML Pipelines
- Storing large training datasets (especially with Lustre).
- Shared storage for distributed training.
- Running ML workloads in hybrid environments (on-prem + cloud).

👉 FSx lets you choose the right file system **for your workload** while staying managed, scalable, and fast.

---

# Amazon FSx for Lustre

## 💡 What is Lustre?
Lustre is a **high-performance parallel file system** used in supercomputers and large-scale ML/data workloads.

## 🔍 Key FSx Lustre Features
- Integrates with **Amazon S3** – You can link an FSx Lustre file system to an S3 bucket.
- Ideal for **ML training jobs** that need fast I/O.
- Offers **millions of IOPS** and **hundreds of GB/s throughput**.
- POSIX-compliant, ideal for Linux-based workloads.

## 🎯 Best Use Cases
- ML training (with large datasets)
- Genomics, financial modeling, media rendering
- Parallelised ML workloads that need fast file access

---

# Amazon FSx for Windows File Server

## 💡 What is It?
A managed file system for **Windows-based workloads** that require NTFS, SMB protocol, and Active Directory support.

## 🔍 Key Features
- Native support for **SMB** protocol and **Windows ACLs**.
- Integrates with **Microsoft AD** (either AWS Managed or self-managed).
- Optimised for Windows-based analytics, apps, and ML tools that need Windows-native storage.

## 🎯 Best Use Cases
- Windows-based ML tools
- Enterprise apps that need file sharing across Windows systems
- Shared storage in hybrid (on-prem + AWS) environments

---

# Amazon FSx for NetApp ONTAP

## 💡 What is It?
Fully managed NetApp ONTAP file systems in AWS, ideal for enterprises already using NetApp.

## 🔍 Key Features
- Supports **NFS, SMB, and iSCSI**
- Snapshots, clones, data deduplication, compression
- Ideal for hybrid setups (on-prem NetApp + AWS)

## 🎯 Best Use Cases
- Enterprise workloads needing advanced storage features
- App migration from on-prem NetApp to AWS
- Scenarios where snapshot, tiering, and cloning are important

---

# Amazon FSx for OpenZFS

## 💡 What is It?
Managed ZFS-based file system built for **Linux/Unix workloads** needing advanced features.

## 🔍 Key Features
- POSIX-compliant, supports NFS
- Snapshots, cloning, checksums, inline data compression
- High throughput with low-latency performance

## 🎯 Best Use Cases
- Linux-based ML applications
- Software development with ZFS familiarity
- Scenarios where advanced file system features are needed

---

✅ These are the **exam-ready, clean notes** you'll want in GitHub to revise FSx effectively.
