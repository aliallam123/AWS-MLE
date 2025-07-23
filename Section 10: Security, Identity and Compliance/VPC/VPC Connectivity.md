# AWS VPC Connectivity – Peering, Endpoints, VPN, Direct Connect

## 🌐 VPC Peering

- Connects **two VPCs privately**, like they’re on the same network
- Works **within or across accounts/regions**
- **Not transitive** — if A peers with B and B peers with C, **A cannot talk to C**
- IP ranges must be **non-overlapping**

---

## 🔌 VPC Endpoints

Allow **private access** to AWS services without using the public internet.

| Type               | Description                                  | Services              |
|--------------------|----------------------------------------------|-----------------------|
| **Gateway Endpoint**   | Targets S3 and DynamoDB                    | ✅ S3, DynamoDB        |
| **Interface Endpoint** | Creates a private ENI in your subnet       | ✅ Most AWS services   |

✅ **Use when:** EC2 or SageMaker inside a private subnet needs access to AWS services like S3, DynamoDB, CloudWatch, etc.

---

## 🛡️ On-Premises Connectivity

| Option              | Description                                           | Internet Used? | Setup Time      |
|---------------------|-------------------------------------------------------|----------------|------------------|
| **Site-to-Site VPN**| Encrypted tunnel over public internet                 | ✅ Yes         | Fast (minutes)   |
| **Direct Connect**  | Physical private connection to AWS                    | ❌ No          | Slower (weeks+)  |

---

## ✅ Exam Essentials

- **VPC peering** = private link between VPCs (non-transitive, IPs must not overlap)
- **VPC endpoint** = private access to AWS services from a VPC
  - **Gateway** → only S3 and DynamoDB  
  - **Interface** → all other services
- **Use VPC endpoint** to access S3 from a private subnet with **no internet access**
- **VPN** = fast, encrypted, over the internet  
- **Direct Connect** = slow setup, but private and high performance
