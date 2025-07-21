# SageMaker Custom Containers & Production Variants

## 🐳 SageMaker and Docker

- SageMaker uses **Docker containers** to run both training and inference jobs.
- Containers must follow specific file structure:
  - `/opt/ml/code` → training script
  - `/opt/ml/input` → input data and configs
  - `/opt/ml/output` → logs and outputs
  - `/opt/ml/model` → model artifacts for inference
- Containers are stored in **Amazon ECR**.

## 📦 Docker Components

- **Dockerfile** defines how the image is built (e.g., `FROM tensorflow`, `pip install`).
- **Important Env Vars**:
  - `SAGEMAKER_PROGRAM`: entrypoint script.
  - `MODEL_DIR`: where checkpoints are saved.
  - `SM_CHANNEL_TRAIN`, `SM_CHANNEL_VALIDATION`: data sources.
  - `HYPERPARAMETERS`: tuning config (used in SageMaker AMT).

## ⚖️ Production Variants (A/B Testing)

- Run multiple model versions in parallel using **variant weights** (e.g., 90% old model, 10% new).
- Useful for testing real-world performance (e.g., recommender systems).
- You can dynamically **adjust weights** or rollback to a known-good model version.

## ✅ Exam Essentials

- Custom containers must be ECR-registered and structured per SageMaker expectations.
- `/opt/ml/code` → training script location (important to remember).
- Use **production variants** for **live A/B testing** of model versions with weighted traffic.
- Variant weights = % of requests routed to each model variant.

## 🎯 Quick Tips

- Custom logic → Custom container in ECR.
- Mention of variant weights = production variants.
- Recommender systems with unpredictable offline performance? → Production variant testing helps.
