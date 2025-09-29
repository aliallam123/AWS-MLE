# SageMaker Inference Deployment Options

## 🚀 Model Deployment Methods

- **JumpStart**: 1-click deployment of pre-trained models using templates.
- **Python SDK (Model Builder)**: Configure deployment settings in code.
- **CloudFormation**:
  - Best for repeatable, CI/CD-driven deployment.
  - Use resource type: `AWS::SageMaker::Model`.

## 🔮 Inference Types

### 1. Real-time Inference
- Best for low-latency, interactive apps (e.g., fraud detection).
- Always-on; suitable for **steady traffic**.
- Higher cost due to persistent resources.

### 2. Serverless Inference
- Ideal for **spiky workloads** or **idle time**.
- Saves cost during idle periods.
- Introduces **cold start** latency during startup.

### 3. Asynchronous Inference
- For **large payloads** or **long processing times**.
- Suitable for non-blocking applications.
- Responses returned when ready (not instantly).

## ⚙️ Auto Scaling

- SageMaker auto scaling adjusts instance count based on metrics.
- Works per **production variant**.
- Uses CloudWatch metrics (e.g., invocations per instance).

## 🧠 SageMaker Neo

- Compiles models for optimized inference (e.g., **Inferentia chips**).
- Improves performance for edge and cloud environments.
- Works with popular frameworks (TF, PyTorch, MXNet, etc.).

## ✅ Exam Essentials

- **JumpStart** = easiest way to deploy pre-trained models.
- **CloudFormation** = best for automation/CI-CD (`AWS::SageMaker::Model`).
- **Real-time** = lowest latency.
- **Serverless** = cost-efficient for idle traffic; risk of cold starts.
- **Async** = best for large, long-running requests.
- **Neo** = optimises inference for performance and edge compatibility.

## 🎯 Quick Tips

- Spiky traffic + cost-conscious? → Serverless.
- Big payloads or slow models? → Asynchronous.
- Fast answers needed? → Real-time inference.
- Deployment automation? → Use CloudFormation.
- Want inference speed boost? → Use SageMaker Neo.
