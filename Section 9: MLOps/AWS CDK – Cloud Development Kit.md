# AWS CDK – Cloud Development Kit

## 💡 What Is CDK?

- **AWS CDK** allows you to define cloud infrastructure using **real programming languages**.
- Supported languages: **TypeScript**, **Python**, **Java**, **.NET**.
- It **compiles code into CloudFormation templates** using `cdk synth`.
- Deployed via `cdk deploy`.

---

## ⚙️ How It Works

1. Write infra in code (e.g., define VPC, ECS, Lambda, S3, etc.)
2. Run `cdk synth` → generates CloudFormation template
3. Run `cdk deploy` → deploys infra using CloudFormation engine

---

## 🧱 Benefits Over Raw CloudFormation

| Feature                  | CloudFormation | CDK                            |
|--------------------------|----------------|--------------------------------|
| Language                 | YAML/JSON      | Real programming languages     |
| Type Safety              | ❌              | ✅                              |
| Logic (loops, conditionals) | ❌          | ✅                              |
| Integration with app code| Limited         | Strong                         |

---

## 📦 CDK vs SAM

| Feature               | AWS CDK                        | AWS SAM                         |
|------------------------|-------------------------------|----------------------------------|
| Language Support        | Python, TS, Java, .NET         | YAML/JSON                        |
| Target Use Case         | Any AWS service                | Serverless apps (Lambda-focused)|
| CloudFormation Backend  | ✅                             | ✅                                |
| Local Testing           | Use with `sam local` after `cdk synth` | ✅                            |

---

## 🧪 Combined Use Case

- CDK defines app infrastructure (e.g., S3 → Lambda → Rekognition → DynamoDB).
- CDK generates the CloudFormation template.
- SAM CLI can be used to test Lambda locally via `sam local invoke`.

---

## ✅ Exam Essentials

- CDK is for **developers** who want to define AWS infra in **code**.
- **Compiles to CloudFormation**, which does the actual provisioning.
- More powerful, testable, and reusable than raw YAML templates.
- **Ideal for teams** building full app infrastructure and wanting full IaC control.

## 🎯 Quick Tips

- “Infra as code using TypeScript/Python?” → **CDK**
- “Compiles to CloudFormation template?” → **CDK**
- “Easier than raw YAML, supports logic?” → **CDK**
- “Want to test Lambda locally from CDK?” → Use `cdk synth` + `sam local`
