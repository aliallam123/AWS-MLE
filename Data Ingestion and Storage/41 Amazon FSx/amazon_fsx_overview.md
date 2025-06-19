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





