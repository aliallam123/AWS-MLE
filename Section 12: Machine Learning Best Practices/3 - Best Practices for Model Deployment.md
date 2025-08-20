# Model Deployment Best Practices – AWS MLE-A Notes

## Core Deployment Flow
1. **Inference Container**
   - Holds inference code + model artifacts (from **Model Registry**) + features (from **Feature Store**).  
   - Deployed as an **endpoint** that applications call for predictions.  

2. **Application Integration**
   - Endpoint consumed by downstream apps.  
   - APIs can be fronted by **API Gateway** for stability.  

---

## Best Practices

### Monitoring & Security
- 📊 Use **CloudWatch, EventBridge, SNS** → monitor endpoints & alerts.  
- 🛡️ Detect drift/adversarial activity → **SageMaker Model Monitor**.  
- 🔐 Protect against malicious input/data poisoning.  

### Automation & Testing
- 🔄 Automate CI/CD deployment → **SageMaker Pipelines**.  
- 🧪 Controlled rollout strategies:  
  - **Blue/Green** → swap old/new endpoints.  
  - **Canary/Linear** → gradually shift traffic.  
  - **A/B Testing** → test multiple models in prod.  

### Deployment Options
- ☁️ **Cloud Inference**:  
  - Real-time endpoints.  
  - Serverless endpoints.  
  - Asynchronous inference.  
  - Batch transform (scheduled).  
- 📱 **Edge Inference**:  
  - **SageMaker Neo**, **AWS IoT Greengrass**.  
  - Useful for low-latency or offline scenarios.  
- ⚙️ Advanced: Multi-model & multi-container endpoints, Inference Pipelines.  

### Cost Optimization
- 💸 Use efficient hardware:  
  - **Inferentia (Inf1/Inf2)** → DL inference.  
  - **Trainium (Trn1)** → model training efficiency.  
  - **Graviton3 CPUs** → general compute efficiency.  
- 📉 Rightsize fleets → **SageMaker Inference Recommender**.  
- ⚡ Auto scaling for endpoints → scale by load.  
- 🧠 Optimize models pre-deployment → **Neo, TreeLite, HuggingFace Infinity**.  
- ♻️ Deploy multiple models behind one endpoint for efficiency.  

### Sustainability & SLAs
- ⚖️ Match deployment strategy to business need:  
