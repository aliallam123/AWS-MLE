# SageMaker Resource Management

## 🧠 Choosing the Right Instance

- **Deep Learning Training** → Use **GPU** instances:
  - G4 (modern)
  - P3 (legacy)
- **Inference** or traditional ML → Use **CPU** instances:
  - C5 (compute-optimised)
  - M5 (general-purpose)

## 💸 Managed Spot Training

- Use **spot instances** to save up to **90%** on training costs.
- Key requirement: Use **S3 checkpoints** to resume if interrupted.
- Tradeoffs:
  - ✅ Save money
  - ❌ Can delay job start (spot capacity wait)
  - ❌ Need extra setup for checkpointing

## ✅ Exam Essentials

- **GPU = training**, **CPU = inference**.
- **Spot training** = cost-effective + risky (interruptions).
- Always pair spot training with **S3 checkpoints**.

## 🎯 Quick Tips

- Deep learning training? → Use G4 or P3.
- Inference only? → Use C5.
- Saving money + large job? → Use spot training with S3 checkpoints.
