# CloudWatch vs CloudTrail vs Config – AWS MLE-A Notes

## Key Differences
- 📊 **CloudWatch** = Performance & monitoring.  
  - Metrics (CPU, network, ELB requests/errors).  
  - Dashboards, alarms, logs.  

- 📹 **CloudTrail** = Activity & governance.  
  - Records **API calls** (who, when, where, what).  
  - Audit trail for changes (e.g., who modified ELB SG rules).  

- 🕵️ **Config** = Compliance & configuration history.  
  - Tracks **resource configurations over time**.  
  - Evaluates compliance against **rules** (e.g., must have SSL cert).  
  - Can trigger remediation actions.  

## ELB Example
- **CloudWatch**: Monitor ELB requests, error rates, latency.  
- **CloudTrail**: Identify **who** changed ELB’s SG or SSL cert.  
- **Config**: Ensure ELB always has SSL cert & blocks unencrypted traffic.  

---

## 🔑 Exam Tips
- 🎥 CloudTrail answers: **“Who did what, when, from where?”**  
- 📊 CloudWatch answers: **“How is it performing right now?”**  
- 🕵️ Config answers: **“Is it compliant with my rules? What changed over time?”**  
- 💡 They are **complementary** — often exam questions ask you to pick the one that best fits the use case.  

---
