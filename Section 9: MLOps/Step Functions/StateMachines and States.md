# AWS Step Functions – State Types Explained

## 🧠 Core Concept

- **Step Functions** let you define **state machines**, which are workflows made of **states**.
- Each **state** does something: runs logic, makes a decision, waits, or ends the workflow.

---

## 🧱 Common State Types

| State Type       | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| **Task**         | Runs work (Lambda, SageMaker, Batch, ECS, API call, etc.)                   |
| **Choice**       | Conditional branching logic (if/else-style)                                 |
| **Wait**         | Adds a time delay between states                                            |
| **Parallel**     | Runs multiple branches of logic at the same time                            |
| **Map**          | Iterates over a dataset and applies logic to each item (parallel by default)|
| **Pass**         | Passes input to output unchanged (for debugging or scaffolding)             |
| **Succeed**      | Marks successful end of workflow                                            |
| **Fail**         | Ends workflow with failure                                                  |

---

## 🔀 Parallel vs Map – Know the Difference

| Feature      | **Parallel**                            | **Map**                                            |
|--------------|------------------------------------------|----------------------------------------------------|
| Purpose      | Run different branches of logic in parallel | Run same logic for each item in a collection        |
| Use Case     | Start Lambda + ECS + Batch together       | Process each row in a file independently            |
| Parallelism  | Manual structure                         | Automatic for each item                             |

---

## ✅ Exam Essentials

- Step Functions = Orchestrate workflows across AWS services
- Know **each state type**, especially **Map** and **Parallel**
- Workflows are written in **Amazon States Language (ASL)** but you won't need to code it in the exam
- **Map** = per-item logic  
- **Parallel** = run different paths together  
- Visual, auditable, long-lived, and fault-tolerant

## 🎯 Quick Tips

- “Orchestrate multiple services?” → Step Functions
- “Repeat steps for each object in S3?” → Use **Map**
- “Run 3 different branches at once?” → Use **Parallel**
- “Handle failure/retry outside of code?” → Step Functions with **Task + Fail + Retry**
