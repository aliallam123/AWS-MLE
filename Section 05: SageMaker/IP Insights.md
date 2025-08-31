# 📘 IP Insights — What You Need to Know for the MLE-A Exam

| **Aspect**              | **What to Know**                                                            |
| ----------------------- | --------------------------------------------------------------------------- |
| **Type**                | Unsupervised — anomaly detection                                            |
| **Use Case**            | Detects suspicious IP activity (e.g. unusual logins, access patterns)       |
| **Input Format**        | CSV only → `entity_id`, `ip_address` (2 columns)                            |
| **Core Mechanism**      | Neural network that embeds entity–IP pairs and detects outliers             |
| **Negative Sampling**   | Auto-generates fake (random) IP/entity pairs to learn anomalies             |
| **Key Hyperparameters** | `num_entity_vectors`, `vector_dim`, `epochs`, `learning_rate`, `batch_size` |
| **GPU Use**             | ✅ Recommended for training (e.g. `p3.2xlarge`), can use multi-GPU           |
| **CPU Use**             | Optional — depends on data size; slower                                     |


# ✅ Exam Tip
If the question mentions IP address anomaly detection, fraud-like patterns, or suspicious logins,
✅ Choose IP Insights
