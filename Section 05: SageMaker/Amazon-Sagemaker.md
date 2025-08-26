# 🚀 Amazon SageMaker – Built-in Algorithms (Section 5 Summary)

## 🧠 What is SageMaker?
Amazon SageMaker is AWS’s end-to-end machine learning platform. It supports the full ML lifecycle:

1. **Data Prep**
2. **Model Training**
3. **Model Evaluation**
4. **Model Deployment**
5. **Monitoring + Retraining**

---

## 🛠️ Core Capabilities

- **Training Data**: Stored in **Amazon S3**
- **Training Code**: Stored as **Docker images in Amazon ECR**
- **Training Compute**: Runs on **EC2** instances
- **Inference Code**: Separate Docker image for predictions
- **Notebook Instances**: Jupyter notebooks with libraries like `scikit-learn`, `PyTorch`, `TensorFlow`
- **Built-in Algorithms**: Prebuilt Docker images for common ML models
- **Hyperparameter Tuning**: Via **Automatic Model Tuning (AMT)**

---

## 🧪 Data Preparation

- **Preferred format**: `RecordIO-Protobuf` (efficient), but **CSV** also works
- **Input Sources**:
  - S3 (default)
  - Athena
  - Redshift
  - EMR
  - Amazon Keyspaces
- **Processing tools**:
  - Pandas / Numpy
  - Spark (via EMR)
  - Scikit-learn
  - Docker containers (custom pre-processing logic)

---

## 📦 Training Jobs

- **Input**: S3 path to training data
- **Output**: S3 path for trained model
- **Training Code**: Docker image in ECR
- **Options**:
  - Built-in SageMaker algorithms
  - Custom Python/TensorFlow/MXNet/PyTorch code
  - Hugging Face models
  - Spark MLlib
  - Bring your own container (BYOC)

---

## 📤 Deployment Options

- **Real-time Inference**: Persistent SageMaker endpoint (low latency)
- **Batch Transform**: One-off predictions on large datasets
- **SageMaker Neo**: Deploy to edge devices
- **Auto Scaling**: Endpoint scaling based on demand
- **Shadow Testing**: Safely test new models vs. current ones before rollout

---

## 🔁 Workflow Management

- Use **notebooks** or **SageMaker console** to:
  - Spin up training jobs
  - Tune models
  - Deploy endpoints
- Automate with:
  - **SageMaker Pipelines**
  - **EventBridge**
  - **CI/CD tools**

---

## 🐳 What is a Docker Image?

A **Docker image** is a portable, ready-to-run package that includes:
- Your **code**
- Runtime (Python, etc.)
- Libraries & dependencies
- OS-level tools

In SageMaker, Docker images are used for:
- Training jobs
- Inference endpoints

Think of it like a **"box"** containing your ML logic, ready to deploy anywhere!

---
