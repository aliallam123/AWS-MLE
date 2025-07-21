# SageMaker Deployment Safeguards (Blue/Green + Shadow Testing)

## 🚦 Deployment Guardrails

SageMaker supports **deployment guardrails** to safely roll out new model versions to endpoints (real-time or async). These include:

### 🔁 Deployment Strategies:
- **All-at-Once**: Entire traffic switched instantly → Monitor → Terminate old model.
- **Canary**: Small % of traffic to new model → Monitor → Full switch if successful.
- **Linear**: Gradual traffic increase in steps → Allows continuous monitoring.
- **Auto-Rollback**: If issues arise, traffic rolls back to old model automatically.

## 🕵️‍♂️ Shadow Testing

- Sends **copy of real traffic** to shadow (test) variant.
- Does **not affect** live inference.
- Used for **manual monitoring** in SageMaker console.
- **Manual promotion** to production if results are satisfactory.

## ✅ Exam Essentials

- Guardrails apply to both **real-time** and **async** endpoints.
- **Shadow testing** ≠ automatic. It's for manual evaluation.
- **Auto-rollback** only applies to **guardrail** strategies (not shadow testing).

## 🎯 Quick Tips

- Canary = small traffic + auto rollback.
- Linear = gradual rollout.
- Shadow = duplicate traffic + manual promotion.
- If the question mentions “observing a model before replacing the old one”, think **Canary or Shadow** depending on automation.

