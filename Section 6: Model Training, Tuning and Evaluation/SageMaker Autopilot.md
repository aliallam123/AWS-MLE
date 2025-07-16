# SageMaker Autopilot – AWS MLE-A Exam

## 🧠 What It Does

- Fully managed **AutoML service**
- Automates:
  - **Data preprocessing**
  - **Model selection**
  - **Hyperparameter tuning**
  - **Deployment-ready model creation**
- Works with **tabular data** (CSV, Parquet)

## 📊 Supported Problem Types

- Binary classification
- Multiclass classification
- Regression

---

## 🚀 Training Modes

| Mode      | When It's Used                          | How It Works                            |
|-----------|------------------------------------------|------------------------------------------|
| **HPO**   | Data > 100MB OR unknown data size        | Tunes hyperparams (Linear, XGBoost, DL)  |
| **Ensemble** | Data < 100MB                          | Combines top models via AutoGluon        |
| **Auto**  | Autodetects based on data size           | HPO if size unknown (e.g. VPC, manifest) |

🔹 HPO uses:
- **Bayesian optimisation** (<100MB)
- **Multi-fidelity optimisation** (>100MB)

🔹 Ensemble uses:
- 10 diverse models + **stacked ensemble**

---

## 🧪 Key Features

### 🧠 Human Control
- Generates **notebooks + model leaderboard**
- You can refine models manually

### ✅ Early Stopping
- Enabled by default
- Stops poor training jobs early (deep learning only)

### 🔁 Warm Start
- Resume failed tuning jobs or reuse config
- Modes: `IdenticalDataAndAlgorithm`, `TransferLearning`

---

## 🛑 Limitations

- Defaults to **HPO** if:
  - S3 data inside **VPC**
  - Using **manifest files**
  - S3 URI has >1000 objects

---

## 🔍 Ethics & Transparency

### 🧩 Integrates with SageMaker Clarify
- Analyses **feature attribution** (via **SHAP** values)
- Detects potential **bias** in predictions
- Supports compliance and auditing

---

## 🧠 Exam Tips

- "AutoML in SageMaker" → **Autopilot**
- "No code" or "CSV in S3" + target column → **Autopilot setup**
- "Bias or transparency in AutoML" → **Clarify integration**
- "Stacking models" → **Ensembling mode**
- "Tunes models + selects best algo" → **HPO mode**
- "Large data + efficient tuning" → **multi-fidelity optimisation**
