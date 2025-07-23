# AWS VPC – Summary for MLE Associate Exam

## 🧠 Core Concept

A **VPC (Virtual Private Cloud)** is your own isolated network in AWS. Every region has a **default VPC**, and resources like EC2 and SageMaker run inside it.

---

## 🌐 Subnets

- **Public Subnet**: Has a route to the **Internet Gateway (IGW)**
- **Private Subnet**: No route to internet, used for internal workloads
- Subnets are **AZ-scoped** (Availability Zone)

---

## 🔌 Internet Access

| Resource         | Used For                             | Notes                        |
|------------------|---------------------------------------|------------------------------|
| **Internet Gateway** | Internet access for public subnets | Attached at the VPC level    |
| **NAT Gateway**     | Outbound access for private subnets | Deployed in public subnet    |

---

## 🧱 Network Security

| Firewall Type     | Scope            | Rules        | Notes                        |
|-------------------|------------------|--------------|------------------------------|
| **Security Group**| EC2/ENI          | Allow only   | **Stateful**                 |
| **NACL**          | Subnet           | Allow & Deny | **Stateless**                |

---

## 🔄 Connectivity Between VPCs

- **VPC Peering**: Connect two VPCs privately
  - **Non-transitive**
  - **No overlapping IPs allowed**

---

## 🧩 VPC Endpoints

- Allow **private access to AWS services** from within a VPC
- Two types:
  - **Gateway Endpoint** → for **S3** and **DynamoDB**
  - **Interface Endpoint** → for other AWS services

---

## 🌍 On-Premises Connectivity

| Method             | Internet Used? | Setup Speed | Description                          |
|--------------------|----------------|-------------|--------------------------------------|
| **Site-to-Site VPN** | ✅ Yes         | Fast        | Encrypted connection over internet   |
| **Direct Connect**   | ❌ No          | Slow        | Private physical link to AWS         |

---

## 📊 VPC Flow Logs

- Capture **IP traffic metadata** for:
  - VPC, subnet, or ENI
- Used for **troubleshooting** and **auditing**
- Logs can go to:
  - **S3**
  - **CloudWatch Logs**
  - **Kinesis Firehose**

---

## ✅ Exam Essentials

- Know difference between **public** and **private** subnets
- **Security Groups** = instance-level, **stateful**
- **NACLs** = subnet-level, **stateless**
- Use **VPC endpoint** for private access to AWS services like S3
- **VPC peering is NOT transitive**
- Flow logs help debug denied network traffic
- **Site-to-Site VPN** = fast, encrypted internet link  
- **Direct Connect** = slower setup, but private and reliable
