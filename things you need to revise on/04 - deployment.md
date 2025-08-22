# Safe Deployment & Testing Strategies (AWS MLE Associate)

## 🔵 Blue/Green Deployment
- Two identical environments: **Blue = current**, **Green = new**  
- Shift **100% of traffic** to Green when ready  
- **Rollback:** fast (switch back to Blue)  
- **AWS:** SageMaker endpoints, CodeDeploy  

## 🟡 Canary Deployment
- Release new version to a **small % of traffic** (e.g., 5%)  
- Monitor metrics → gradually increase until 100%  
- **Good for ML:** catches regressions early  

## 🟠 Linear Deployment
- Similar to canary, but increases traffic in **fixed increments** (e.g., +20% every 10 min)  
- Automated, predictable rollout  

## 🟣 Shadow (Mirroring) Testing
- Send **duplicate requests** to both old & new models  
- Only **old model’s output** returned to users  
- New model’s responses are **logged & analysed**  
- **Use case:** validate safety, drift, performance without user impact  

## 🟢 A/B Testing
- Split **real user traffic** between models (e.g., 80% model A, 20% model B)  
- Users actually see different versions  
- Goal: compare **business KPIs** (CTR, conversions, latency)  
- **AWS:** SageMaker multi-variant endpoints  

## ⚡ Traffic Splitting in SageMaker
- SageMaker endpoints allow custom traffic routing:  
  - Variant A (80%), Variant B (20%), etc.  
- Supports canary, A/B, gradual rollouts  

---

## ✅ Key Differences
- **Blue/Green:** full swap, instant rollback  
- **Canary:** gradual rollout with small initial traffic  
- **Linear:** predictable incremental rollout  
- **Shadow:** new model tested silently, no user impact  
- **A/B:** compare live model performance on real traffic  

---

## 📝 Exam Tips
1. **Look for hints in scenarios:**  
   - “Shift 10% traffic” → Canary/Linear  
   - “Run in parallel, no customer impact” → Shadow  
   - “Instant rollback required” → Blue/Green  
   - “Compare business outcomes” → A/B  

2. **SageMaker endpoints** = main service for safe ML deployments  

3. **Rollback:** Blue/Green best for quick switchback  

4. **Monitoring:** Use CloudWatch, SageMaker Model Monitor, Clarify for drift & bias detection  

---
