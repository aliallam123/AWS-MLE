# Model Development Best Practices – AWS MLE-A Notes

## Core Stages
1. **Algorithm Selection**
   - Choose the simplest algorithm that solves the problem (don’t default to deep learning).  
   - Evaluate tradeoffs: accuracy vs complexity, precision vs recall, bias vs fairness.

2. **Training**
   - Use **SageMaker Training Jobs** (local for small datasets, cloud for scale).  
   - Speed up with **distributed training** (data parallel for big datasets, model parallel for large models).  
   - Enable **debugging & logging** → **SageMaker Debugger + CloudWatch**.  
   - Apply **early stopping** to avoid wasted compute.

3. **Hyperparameter Tuning**
   - Automate with **SageMaker Automatic Model Tuning (AMT)**.  
   - Prefer **Bayesian / Hyperband** → more efficient than grid/random search.  
   - Warm start + checkpointing for iterative jobs.

4. **Evaluation & Validation**
   - Track experiments → **SageMaker Experiments**.  
   - Validate models → **SageMaker Model Monitor**.  
   - Check fairness/bias → **SageMaker Clarify**.  
   - Use **QuickSight** for visualization.

5. **Model Packaging & Versioning**
   - Store versions → **SageMaker Model Registry**.  
   - Ensure feature consistency with **Feature Store**.  
   - Manage containers/deps → **ECR**, **CodeArtifact**.

---

## MLOps & Automation
- Automate pipelines → **SageMaker Pipelines, Step Functions, CloudFormation, CDK**.  
- CI/CD for ML → traceable, reproducible builds.  
- Secure inter-node comms → **SageMaker inter-node encryption, EMR in-transit encryption**.  
- Rollback via Model Registry + Feature Store in case of data poisoning.

---

## Cost & Sustainability
- ⚡ Optimize instance size → max single-instance before scaling out.  
- 💸 Use **Spot Instances** for training (via SageMaker Managed Spot).  
- 📉 Stop idle resources → SageMaker lifecycle configs, Studio auto-shutdown.  
- 🔔 Set **AWS Budgets + Cost Explorer** for monitoring.  
- 🌱 Select energy-efficient regions (green power).  
- 🧹 Archive/delete unused artifacts.  
- 🎯 Define “good enough” criteria → don’t overtrain.  

---

## Best Practices Summary
- 🧪 Use **Experiments** to compare training runs.  
- 🔍 **Clarify** for bias + fairness, **Debugger** for convergence issues.  
- 🗂️ **Model Registry** for reproducibility/versioning.  
- 📊 **Model Monitor** for post-deployment validation.  
- 🚀 **Autopilot** for AutoML when appropriate.  
- 🔄 Prefer pre-trained models (JumpStart, Bedrock) → reduce cost & time.  
- ✅ Limit concurrent training jobs, focus only on key hyperparameters.  

---

## 🔑 Exam Tips
- **AMT** = hyperparameter tuning.  
- **Experiments** = compare training/eval runs.  
- **Debugger** = diagnose training failures.  
- **Model Registry** = reproducibility/version control.  
- **Model Monitor** = monitor drift & quality.  
- **Clarify** = bias + explainability.  
- **Budgets/Cost Explorer** = cost control for ML training.  
- 🛑 Always optimize for cost, sustainability, and simplicity in algorithm choice.  

---
