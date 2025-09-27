# SageMaker Neo and Edge Inference

## 🧠 What Is Neo?

- **SageMaker Neo** compiles ML models to run efficiently on **edge devices** (e.g., smart cameras, cars).
- Supports models trained with **TensorFlow, PyTorch, MXNet, ONNX, XGBoost**.
- Optimizes for various chip architectures: **ARM, Intel, Nvidia**.
- Key benefit: **Train once, run anywhere** – low latency, local inference.

## 🔄 Neo Workflow

1. Train model in **SageMaker** (cloud).
2. Compile using **Neo Compiler**.
3. Deploy to edge using **AWS IoT Greengrass**.
4. **Neo Runtime** runs compiled model on device.

## 📦 Why Use Neo?

- **Local inference** removes internet latency (essential for self-driving cars, smart devices).
- Can also host compiled models on EC2 (if architecture matches), but **edge deployment is key use case**.

## 🧩 Key Integrations

- **AWS IoT Greengrass**:
  - Deploys compiled models to edge devices.
  - Uses **Lambda functions** to run inference locally.
- **Lambda on edge + Neo + Greengrass** often appear together in edge ML architectures.

## ✅ Exam Essentials

- Neo = compiler + runtime for edge.
- Greengrass = model deployment to device.
- Supports a wide range of frameworks.
- Compiled model must match device type (e.g., ARM → ARM).

## 🎯 Quick Tips

- Latency-sensitive + local = Neo + Greengrass.
- Model compilation = Neo.
- Deployment mechanism = Greengrass.
- Lambda often powers edge inference logic in this setup.
