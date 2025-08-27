# 📘 SageMaker Built-in Algorithm: XGBoost (Exam Revision)

## ✅ Overview
- **Type**: Ensemble method (Gradient Boosted Decision Trees)
- **Use Cases**: 
  - Regression
  - Binary classification
  - Multi-class classification
  - Ranking
- **Available as**: Built-in algorithm in SageMaker

---

## 📥 Input Format & Modes
- **Supported formats**: 
  - CSV
  - LibSVM
- **Input Modes**:
  - `File` (copies full dataset to instance)
  - `Pipe` (streams from S3; preferred for large datasets)

---

## ⚙️ Key Features
- Boosted trees trained sequentially
- Supports sparse input and missing values
- High performance on structured/tabular data
- Uses level-wise tree growth (parallelisable)

---

## 🎛️ Important Hyperparameters

### 🔹 Model Complexity
- `max_depth`: max depth of trees (controls overfitting)
- `min_child_weight`: min sum of instance weight in a child
- `gamma`: min loss reduction to make a split
- `subsample`: row sampling ratio
- `colsample_bytree`: feature sampling ratio

### 🔹 Training Control
- `eta`: learning rate (lower = more robust)
- `num_round`: number of boosting rounds
- `early_stopping_rounds`: stops training if no improvement

### 🔹 Regularisation
- `lambda`: L2 regularisation (default = 1)
- `alpha`: L1 regularisation (default = 0)

### 🔹 Objective Functions
- `reg:squarederror`: regression
- `binary:logistic`: binary classification
- `multi:softprob`: multi-class classification (probabilities)

---

## 🧪 Evaluation Metrics
- Regression: `RMSE`, `MAE`
- Classification: `AUC`, `logloss`, `error`, `accuracy`

---

## 🛠️ SageMaker Specifics
- Built-in in SageMaker (`xgboost` container)
- Supports automatic model tuning (hyperparameter optimisation)
- Training & batch inference supported

---

## 💻 Instance Support
- Supports both CPU & GPU
- Scales across multiple instances

---

## 📝 Exam Tips
- Best choice for **structured/tabular** data
- Know which **hyperparameters** reduce overfitting (`gamma`, `subsample`, `lambda`, `alpha`)
- Use `Pipe mode` for large data
- Select correct `objective` based on problem type
