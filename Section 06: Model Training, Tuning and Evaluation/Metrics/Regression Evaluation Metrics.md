# Regression Evaluation Metrics – AWS MLE-A Exam

## ✅ Answering Strategy (Cheat-Sheet Style)

### 📉 RMSE (Root Mean Squared Error)
- Look for: **"Penalise large errors more"**, **"Sensitive to outliers"**
- Use when large prediction errors are especially bad

### 📉 MAE (Mean Absolute Error)
- Look for: **"Treat all errors equally"**, **"Robust to outliers"**
- Use when all errors should be treated the same, even big ones

### 📊 R² (R-squared)
- Look for: **"How well do predicted values explain variance?"**
- Measures **goodness-of-fit** → 1.0 = perfect, 0 = no explanatory power

## 🧠 Tips for the Exam

- Use **RMSE** when the cost of large errors matters more
- Use **MAE** when you want a simple, consistent measure of error
- **R² is only for regression**, never classification
- If the question involves **predicting a number** (price, score, value) → think RMSE / MAE / R², not precision/recall
- RMSE > MAE → more sensitive to outliers

## ❌ Don’t Use

- Classification metrics like **F1**, **Precision**, **Recall**, or **Accuracy** for numeric predictions
