# 📘 SageMaker Built-in Algorithm: Factorization Machines

## ✅ Overview
- **Type**: Supervised (classification & regression)
- **Use Case**: Works best with **sparse data**, especially in **recommendation systems**, click prediction, or any high-dimensional user/item interaction.

## 📥 Input Format
- **Only** supports **RecordIO‑Protobuf** (`float32`)
- Not suitable for CSV due to sparsity of large feature spaces

## 🎯 Core Idea
- Models **pairwise interactions** (e.g. user–item) via matrix factorization
- Learns latent feature representations (`num_factors`) + bias + linear terms

## 🔧 Key Hyperparameters
- `feature_dim`: input feature dimension (e.g. # of items + users)
- `num_factors`: latent dimension size (start ~64)
- `predictor_type`: `binary_classifier` or `regressor`
- Optional knobs: `mini_batch_size`, `epochs`, and learning rates (`bias_lr`, `linear_lr`, `factors_lr`)

## 💻 Instance Support
- Preference: **CPU** — ideal for sparse data
- **GPU** only helps with dense data (rare in real use cases)
- Supports multi-instance distributed training

## 📝 Exam Tips
- Choose Factorization Machines for **sparse supervised learning** (especially recommendations)
- Always use **RecordIO‑Protobuf**
- Focus on tuning:
  - `num_factors` to balance model complexity vs sparsity
  - Adjust **learning rates** and **batch size**
- Use CPU instances for cost-effective training

