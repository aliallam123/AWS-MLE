# AWS CodePipeline – CI/CD Orchestration on AWS

## 🔄 What Is CodePipeline?

- **AWS CodePipeline** automates and orchestrates the steps of **continuous integration and delivery (CI/CD)**.
- Connects services like:
  - **CodeCommit** → Source control
  - **CodeBuild** → Build/test
  - **CodeDeploy / Beanstalk / CloudFormation** → Deployment targets

---

## ⚙️ Key Features

- Fully **managed** and **event-driven**
- Automatically triggers on code changes
- Supports **parallel and sequential actions**
- **Third-party integrations**:
  - GitHub
  - Jenkins
  - Bitbucket
- **Custom actions** via Lambda or plugins

---

## 🧱 Typical Workflow Example

1. **Push code to CodeCommit**
2. **CodePipeline** triggers
3. **CodeBuild** runs unit tests and compiles code
4. **CodeDeploy** deploys artifact to EC2, Lambda, or Beanstalk

---

## 💡 CI/CD Explained

- **CI (Continuous Integration)**:
  - Code is automatically built and tested on commit
- **CD (Continuous Delivery)**:
  - Code is automatically deployed after passing tests

---

## ✅ Exam Essentials

- “Pipeline orchestration” → **CodePipeline**
- Used to connect CI/CD components like:
  - Source (Git/CodeCommit)
  - Build (CodeBuild)
  - Deploy (CodeDeploy/CloudFormation)
- Compatible with custom plugins and 3rd party tools

## 🎯 Quick Tips

- “Automate build → test → deploy?” → **CodePipeline**
- “Manage end-to-end CI/CD in AWS?” → **CodePipeline**
- Works with CodeBuild, CodeDeploy, CloudFormation, and more
