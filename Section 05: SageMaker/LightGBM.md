# 📘 SageMaker Built-in Algorithm: LightGBM (Exam Revision)

## ✅ Overview
- **Type**: Ensemble method – Gradient Boosted Decision Trees (like XGBoost)
- **Use Cases**:
  - Classification
  - Regression
  - Ranking
- **Also similar to**: CatBoost (not covered in depth but same GBDT family)

---

## 📥 Input Format & Modes
- **Format**: Text/CSV only
  - No headers or labels in training files
- **Validation data**: Optional CSV input
- **Input Modes**: File-based only (Pipe mode not mentioned for LightGBM)

---

## ⚙️ Key Features
- Builds on GBDT with:
  - Gradient-based One-Side Sampling
  - Exclusive Feature Bundling
- Ensemble of decision trees (boosted sequentially)
- Memory-bound algorithm (RAM intensive)

---

## 🎛️ Important Hyperparameters

### 🔹 Training Dynamics
- `learning_rate`: controls step size
- `num_leaves`: max number of leaves per tree
- `max_depth`: max tree depth
- `min_data_in_leaf`: min records per leaf (helps reduce overfitting)

### 🔹 Sampling/Regularisation
- `feature_fraction`: % of features used per tree
- `bagging_fraction`: % of data sampled
- `bagging_freq`: frequency of re-sampling

---

## 💻 Instance Support
- **CPU-only**
- Supports:
  - ✅ Single instance
  - ✅ Multi-instance (set via `instance_count`)
- **Best instance type**: General Purpose (e.g., `m5`)
- ❌ Avoid Compute-Optimised (e.g., `c5`) – insufficient memory

---

## 📝 Exam Tips
- Use when asked about **memory-bound GBDT** methods
- Choose **LightGBM** for classification, regression, or ranking
- Pick **general purpose CPUs** over compute-optimised
- Remember it only supports **CSV input** with no headers/labels
- Adjust `min_data_in_leaf` to help mitigate **overfitting`
