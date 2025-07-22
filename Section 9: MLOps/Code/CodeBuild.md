# AWS CodeBuild – Cloud-Based Build Service

## 🔧 What Is CodeBuild?

- **AWS CodeBuild** is a fully managed, serverless build service.
- Used to **compile source code**, **run tests**, and **produce artifacts** ready for deployment.

---

## ⚙️ How It Works

1. Source code is stored in **CodeCommit**, GitHub, or other supported repos.
2. A **buildspec.yml** defines build instructions.
3. CodeBuild:
   - Pulls the code
   - Executes build steps
   - Runs tests
   - Produces deployable artifacts

---

## 🧱 Key Features

- **Serverless & auto-scaling**
- Supports many languages/runtimes (Node.js, Python, Java, Go, etc.)
- Pay-as-you-go: charged per build time
- Fully integrates with:
  - **CodeCommit**
  - **CodePipeline**
  - **CodeDeploy**

---

## 🧪 Use Case Example

- Push code → CodeBuild builds and tests → Artifacts sent to CodeDeploy → Deployed to EC2 or Lambda

---

## ✅ Exam Essentials

- CodeBuild is part of AWS CI/CD suite (with CodeCommit, CodeDeploy, CodePipeline)
- No servers or scaling required — it's **fully managed**
- Triggers builds on code changes
- Outputs build artifacts for further use in the pipeline

## 🎯 Quick Tips

- “Run tests and build app in cloud?” → **CodeBuild**
- “No servers, just builds?” → **CodeBuild**
- “CI/CD build stage on AWS?” → **CodeBuild + CodePipeline**
