# ✅ Key Differences (Exam Ready)

| Feature              | **KNN**                             | **K-Means**                                   |
| -------------------- | ----------------------------------- | --------------------------------------------- |
| **Supervised?**      | ✅ Yes                               | ❌ No                                          |
| **Use Case**         | Predict labels or values            | Cluster unlabeled data                        |
| **Key Hyperparam**   | `k` (neighbors)                     | `k` (clusters), `extra_cluster_center_factor` |
| **SageMaker Bonus**  | Uses index & sampling               | Uses big K & Lloyd’s reduction                |
| **Scaling Strategy** | Sampling + dimensionality reduction | Data sharding (by S3 key)                     |
