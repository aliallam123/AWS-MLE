# SageMaker Serverless Inference & Inference Recommender

## ⚙️ Serverless Inference

- No need to manage infrastructure.
- Define:
  - **Memory** and **concurrency** per container.
- Automatically **scales to zero** when idle.
- Ideal for **infrequent or unpredictable traffic**.
- Billed **per invocation** (cost-efficient for low traffic).
- May introduce **cold start** latency.
- CloudWatch Metrics:
  - `ModelSetupTime`, `Invocations`, `InvocationErrors`, `MemoryUtilization`.

## 🧠 Inference Recommender

- Helps select **optimal instance types and configs** for inference.
- Requires model to be in **SageMaker Model Registry**.
- Provides:
  - **Cost per hour**
  - **Cost per inference**
  - **Latency metrics**

### Modes:
1. **Instance Recommendations**
   - Tests AWS-suggested instances automatically (~45 min).
   - Fast, good for general guidance.

2. **Endpoint Recommendations**
   - Custom test: define your traffic pattern, SLA, instance types (~2 hours).
   - Tailored results for specific needs.

## 🧩 Summary of Inference Options

| Option                  | Best For                         | Control Level     |
|------------------------|----------------------------------|-------------------|
| **Serverless Inference** | Spiky traffic, cost saving       | Low (fully managed) |
| **Auto Scaling**        | Moderate control, steady load     | Medium             |
| **Inference Recommender**| Optimising latency/cost tradeoffs | High (manual tuning) |

## ✅ Exam Essentials

- Serverless: best for **idle traffic**, **scales to 0**, may cold start.
- Recommender:
  - Instance mode = fast auto benchmark.
  - Endpoint mode = SLA-driven custom tests.
- Always monitor with **CloudWatch**.

## 🎯 Quick Tips

- “Scale-to-zero” or “unpredictable traffic” → **Serverless Inference**.
- “Help me choose best instance” → **Inference Recommender**.
- “Custom SLAs or traffic patterns” → Use **Endpoint Recommendation** mode.
