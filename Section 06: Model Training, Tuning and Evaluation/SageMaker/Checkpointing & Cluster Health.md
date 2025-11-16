# 🧠 SageMaker Checkpointing & Cluster Health – GitHub Revision Notes

## 📌 Checkpointing

- **Purpose**: Save training progress periodically to recover from crashes or analyse intermediate states.
- **Default path**: `/opt/ml/checkpoints` — can be customised.
- **Key parameters**:
  - `checkpoint_s3_uri`: S3 path where checkpoints are saved.
  - `checkpoint_local_path`: Local path override (optional).
- **Where to configure**:
  - Programmatically via estimator parameters.
  - In the SageMaker Console UI under *Checkpoint Configuration*.

---

## 🛡️ Cluster Health Checks & Auto-Restarts

- **Instance types**: Automatically enabled on **ML** and **MLP** types.
- **Monitors**:
  - **GPU health**
  - **Nvidia Collective Communication Library (NCCL)** readiness
  - **Internal SageMaker service errors**
- **Behaviour**:
  - Automatically replaces failed GPU instances.
  - Restarts healthy ones.
  - Retries the job without manual intervention.
- **Note**: Great for reliability in large-scale training, but can lead to increased costs.

---

## 💡 Exam Watchouts

- Checkpointing = avoid retraining from scratch.
- Cluster auto-restarts = only on ML/MLP instances, especially helpful for large distributed jobs.
