# AWS CodeDeploy – Hybrid Application Deployment

## 🚀 What Is AWS CodeDeploy?

- A fully managed deployment service for automating app updates on:
  - **EC2 instances**
  - **On-premises servers**
- Supports transitioning applications from **version 1 to version 2**, automatically.

---

## 🧱 Key Characteristics

- **Hybrid**: Works across cloud (EC2) and on-premise environments.
- **Agent-based**: Requires CodeDeploy agent installed on all target servers.
- **Independent**: Does not depend on CloudFormation or Elastic Beanstalk.

---

## ⚙️ Responsibilities

| You Provide                | AWS CodeDeploy Handles                   |
|----------------------------|------------------------------------------|
| Provisioned EC2/on-prem servers | App update orchestration              |
| CodeDeploy agent setup     | Deployment sequencing & rules             |
| Deployment artifacts (e.g. appspec.yml) | Version tracking & rollback support |

---

## 💡 Use Cases

- Consistently deploy application updates across different environments
- Modernize on-prem deployment with AWS tooling
- Simplify EC2 deployments with controlled versioning

---

## ✅ Exam Essentials

- **Works with EC2 and on-prem** — hybrid deployment tool
- Requires **CodeDeploy agent** on target instances
- Not tied to other services like Beanstalk or CloudFormation
- Ideal for companies **transitioning to the cloud**

## 🎯 Quick Tips

- “Deploy to EC2 and on-prem?” → **CodeDeploy**
- “Agent required?” → Yes, on all target machines
- “Not tied to a specific AWS service?” → **Independent deployment tool**
