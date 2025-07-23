# AWS Shield – DDoS Protection

## 🛡️ What Is AWS Shield?

**AWS Shield** is a managed service that provides protection against **DDoS (Distributed Denial of Service)** attacks. These attacks aim to overwhelm and disable your infrastructure by flooding it with traffic. Shield helps mitigate these risks at **Layer 3, 4, and 7**.

---

## 🔰 Shield Standard (Free)

- **Automatically enabled** for all AWS accounts
- Protects against common **Layer 3/4** DDoS attacks:
  - SYN floods
  - UDP floods
  - Reflection attacks
- Applies to services like:
  - **EC2**
  - **CloudFront**
  - **Route 53**
  - **Elastic Load Balancing**

---

## 🛡️ Shield Advanced (Paid)

- ~$3,000/month per org
- Adds protection for **complex and large-scale attacks**
- Protects:
  - EC2
  - ELB
  - CloudFront
  - Route 53
  - Global Accelerator
- Includes:
  - 24/7 access to AWS **DDoS Response Team (DRT)**
  - **Financial protections** against scaling costs from attacks
  - **Auto WAF rule injection** for **Layer 7 (HTTP)** attacks

---

## ✅ Exam Essentials

- **Shield Standard** is always on and free
- **Shield Advanced** = paid service with advanced protections and human support
- Automatically integrates with **WAF** for **Layer 7** attack mitigation
- Commonly tested alongside services like **CloudFront**, **Route 53**, and **Global Accelerator**
