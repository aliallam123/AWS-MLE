# AWS VPC – Networking Basics for ML Engineers

## 🌐 What Is a VPC?

An **Amazon VPC** (Virtual Private Cloud) is a logically isolated **private network** in AWS where you launch resources like **EC2**, **SageMaker**, or **Lambda**. It’s **region-specific** and contains **subnets**, route tables, and gateways that define your network's structure and connectivity.

---

## 🧱 Core Components

### 🧩 Subnets

| Type            | Description                                           |
|------------------|-------------------------------------------------------|
| **Public Subnet** | Has a route to an **Internet Gateway** (IGW) → can access and be accessed by the internet |
| **Private Subnet**| No direct internet access — used for internal-only resources (e.g., DBs, secure EC2) |

---

### 🌉 Gateways

| Gateway Type         | Purpose                                                                 |
|----------------------|-------------------------------------------------------------------------|
| **Internet Gateway** | Enables internet access for public subnets                             |
| **NAT Gateway**      | Lets **private subnets** access the internet **outbound only**          |
| **NAT Instance**     | Self-managed alternative to NAT Gateway (not recommended anymore)        |

---

## 🧭 Routing

- **Route tables** define traffic flow between subnets and the internet
- Public subnets route to the **internet gateway**
- Private subnets route to a **NAT gateway/instance** in a public subnet

---

## 📍 Exam Essentials

- VPC = **region-scoped**
- Subnets = **AZ-scoped**
- Public subnet = has **route to IGW**
- Private subnet = can access internet via **NAT**, but cannot be accessed directly
- NAT Gateway goes in a **public subnet**
- Default VPC (created automatically) contains only **public subnets**
