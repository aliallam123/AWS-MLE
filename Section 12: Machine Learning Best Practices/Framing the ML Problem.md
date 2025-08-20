# Machine Learning Best Practices – AWS MLE-A Notes

## ML Lifecycle (AWS Context)
1. **Data Collection & Prep**  
   - Pre-process, feature engineering.  
   - ✅ Use **SageMaker Feature Store** (online/offline).  
   - ✅ Use **Glue DataBrew** for PII detection, masking, transformation.
  
   - <img width="882" height="389" alt="image" src="https://github.com/user-attachments/assets/b0ac963b-2852-4e83-8727-963d831ca87f" />


2. **Training, Tuning, Evaluation**  
   - Run experiments → **SageMaker Experiments**.  
   - Hyperparameter tuning → **SageMaker Automatic Model Tuning (AMT)**.  
   - AutoML → **SageMaker Autopilot**.  
   - Save versions → **SageMaker Model Registry**.  

3. **Deployment & Inference**  
   - Deploy models via SageMaker endpoints.  
   - Abstract with **API Gateway** → stable API for apps.  
   - Support microservices with **Lambda / Fargate**.  

4. **Monitoring & Feedback Loops**  
   - Model drift/bias → **SageMaker Model Monitor + Clarify**.  
   - Human review → **Amazon A2I** (Augmented AI).  
   - Ops monitoring → **CloudWatch**.  

5. **Governance & Lineage**  
   - Define roles → **SageMaker Role Manager**.  
   - Track pipelines → **SageMaker Lineage + Pipelines**.  

---

## Cost, Sustainability, & Best Practices
- 💰 **Control Costs**  
  - Reuse **pre-trained models** (Bedrock, JumpStart, Marketplace).  
  - Use AutoML to save engineering time.  
  - Compare custom vs pre-trained models → avoid unnecessary training.  

- 🌱 **Sustainability**  
  - Choose greener regions (e.g., US West with hydro).  
  - Optimize compute usage (Spot Instances, right-sized training).  
  - Reduce energy waste by reusing models & fine-tuning instead of training from scratch.  

---

## 🔑 Exam Tips
- 📂 **Model Registry** = versioning + reproducibility.  
- ⚙️ **Automatic Model Tuning** = hyperparameter optimization.  
- 🧪 **Experiments** = compare training runs.  
- 👀 **Clarify** = bias + explainability checks.  
- 🧑‍⚖️ **A2I** = human-in-the-loop evaluation.  
- 🔗 **Config vs ML** → Config = compliance; **SageMaker Role Manager** = ML roles & permissions.  
- 💸 Always evaluate **custom vs pre-trained** for cost & sustainability.  

---
