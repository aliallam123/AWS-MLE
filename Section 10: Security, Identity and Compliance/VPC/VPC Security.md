# VPC Security – NACLs, Security Groups, and Flow Logs

## 🔐 Network Security in a VPC

To protect resources in a **VPC**, AWS provides two main firewall mechanisms:

---

## 🔰 Security Groups

- **Instance-level firewall**
- Attached to **ENIs or EC2 instances**
- Only supports **allow rules**
- Stateful: return traffic is automatically allowed
- Can reference **IP addresses** or **other security groups**
- Default setting in the default VPC: **allow all outbound**, **block all inbound**

---

## 🚧 Network ACLs (NACLs)

- **Subnet-level firewall**
- Support both **allow and deny rules**
- Stateless: return traffic must be explicitly allowed
- Rules are based on **IP addresses only**
- Default NACL in default VPC: allows all in and all out

---

## 📊 VPC Flow Logs

- Captures **IP traffic metadata** for:
  - VPC
  - Subnet
  - ENI (Elastic Network Interface)
- Useful for:
  - **Troubleshooting connectivity issues**
  - **Auditing traffic behavior**
- Can send logs to:
  - **Amazon S3**
  - **CloudWatch Logs**
  - **Kinesis Data Firehose**
- Covers traffic from services like **RDS**, **ElastiCache**, **ELB**, **Aurora**, etc.

---

## ✅ Exam Essentials

- **Security Groups** = instance-level, allow-only, stateful
- **NACLs** = subnet-level, allow + deny, stateless
- **VPC Flow Logs** = for **troubleshooting** network issues
- Flow logs capture **accepted and rejected traffic**
- Logs can be routed to **CloudWatch**, **S3**, or **Firehose**
