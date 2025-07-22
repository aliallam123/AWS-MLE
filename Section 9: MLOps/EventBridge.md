# Amazon EventBridge – Event-Driven Automation on AWS

## 🚦 What Is EventBridge?

- Fully managed **event bus service** that lets you **route, filter, and respond** to events from AWS services, SaaS providers, or your own apps.
- Formerly known as **CloudWatch Events**.

---

## 📬 Types of Event Buses

| Type            | Description                                            |
|-----------------|--------------------------------------------------------|
| **Default**     | Automatically receives events from AWS services       |
| **Partner**     | Events from external SaaS providers (e.g. Zendesk)     |
| **Custom**      | User-defined; send custom app events into AWS         |

---

## 🧱 Key Features

- **Event Filtering**: Match rules based on event patterns
- **Event Destinations**:
  - Lambda, Step Functions, ECS, SQS, SNS, CodeBuild, CodePipeline, EC2 actions, SSM automation
- **Scheduled Events**: Use cron or rate expressions
- **Event Archiving & Replay**:
  - Retain events indefinitely or for set periods
  - Replay events for debugging/failure recovery
- **Schema Registry**:
  - Automatically infers schema from events
  - Generates code bindings in supported languages

---

## 🔐 Permissions

- Supports **resource-based policies** for:
  - **Cross-account event sharing**
  - Centralised event bus patterns in org setups

---

## ✅ Exam Essentials

- "Trigger Lambda when X happens" → **EventBridge**
- "Cron jobs or scheduled jobs in AWS" → **EventBridge**
- Events are **JSON objects**, passed between services
- Use **Schema Registry** for code generation
- Use **custom event buses** for internal application events
- **Supports cross-account** event delivery via resource policies

## 🎯 Quick Tips

- “React to AWS or app events” → **EventBridge**
- “Want to replay/debug past events?” → Use **event archive + replay**
- “Need to route SaaS (e.g., Zendesk) events into AWS?” → Use **partner event bus**
- “Generate code from event format?” → Use **Schema Registry**
