# Ensemble Learning (Bagging vs Boosting) – AWS MLE-A Exam

## 🧠 Key Concepts

### 🟩 Bagging
- Example: **Random Forest**
- Combines multiple models trained on **bootstrapped datasets**
- **Parallel** training
- Helps **reduce overfitting**
- Use when you need **stability + regularisation**

### 🟧 Boosting
- Example: **XGBoost** (popular in SageMaker)
- Models trained **sequentially**, correcting previous errors
- Focuses on **accuracy**
- Can **overfit** if not regularised
- Strong choice when accuracy is most important

## ⚖️ Summary Comparison

| Feature        | Bagging               | Boosting               |
|----------------|------------------------|-------------------------|
| Training Style | Parallel               | Sequential              |
| Goal           | Reduce overfitting     | Maximise accuracy       |
| Overfitting    | Helps prevent it       | Prone if not tuned      |
| Speed          | Faster (parallelizable)| Slower (serial process) |

## 🧪 Exam Tips

- **XGBoost** → Think **boosting + accuracy**
- **Random Forest** → Think **bagging + overfitting**
- Boosting = Better performance, more sensitive
- Bagging = More stable, easier to scale
