# SageMaker Inference Pipelines

## 🔗 What Are Inference Pipelines?

- A way to **chain 2–15 Docker containers** into a single **linear pipeline** for inference.
- Each container performs a step: e.g., **preprocessing → model inference → postprocessing**.
- Containers can include:
  - Built-in SageMaker models
  - Custom Docker containers
  - scikit-learn
  - Spark ML (**EMNLP** serialized format)

## 🧠 Supported Inference Modes

- Works with:
  - **Real-time Inference** (API-based, low latency)
  - **Batch Transform** (bulk inference on large datasets)

## ✅ Exam Essentials

- Use inference pipelines to **modularise your inference logic**.
- Combine **multiple stages** (e.g., text tokenization + model + formatting) into a single API or batch job.
- Spark ML in SageMaker = **EMNLP format**.
- Useful for both **real-time** and **batch** prediction scenarios.

## 🎯 Quick Tips

- "Multiple containers" or "pre/post-processing with model" → Use **inference pipeline**.
- If batch + multiple stages → Inference pipeline supports that.
- Mention of **EMNLP** = Spark ML inside pipelines.
