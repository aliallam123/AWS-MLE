# AWS WAF – Web Application Firewall

## 🛡️ What Is AWS WAF?

**AWS WAF** is a managed **Layer 7** firewall that protects your **web applications** from common HTTP-based attacks like **SQL injection**, **cross-site scripting**, and **DDoS-style floods**. It works by applying **Web ACLs** (access control lists) to supported services and blocking, allowing, or counting requests based on defined rules.

---

## 🧱 Key Features

- Protects against:
  - SQL injection
  - Cross-site scripting (XSS)
  - Rate-based attacks
  - Geo IP blocking
  - Oversized requests
- Supports filtering based on:
  - **IP addresses**
  - **Headers**, **URI**, **Body**
  - **Geo match** and **rate limiting**

---

## 🎯 WAF Deployment Targets (Know for Exam!)

| ✅ Supported Services               | ❌ Not Supported      |
|------------------------------------|------------------------|
| Application Load Balancer (ALB)    | Network Load Balancer (NLB) |
| API Gateway                        |                        |
| CloudFront                         |                        |
| AppSync (GraphQL API)              |                        |
| Cognito User Pools                 |                        |

- Web ACLs are **regional**, except for **CloudFront** (global)
- **Rule groups** help reuse sets of rules across ACLs

---

## 🌍 Fixed IP + WAF

- Use **Global Accelerator** for **fixed IP**
- Front it with an **ALB + WAF** to apply web protections

---

## ✅ Exam Essentials

- WAF is for **Layer 7** (HTTP/S)
- **Not supported** on NLB (Layer 4)
- Deploy on **ALB, API Gateway, CloudFront, Cognito, AppSync**
- **Rate limiting**, **IP filtering**, **geo blocking** are common exam triggers
- Use **Global Accelerator** + ALB to expose a fixed IP with WAF protection
