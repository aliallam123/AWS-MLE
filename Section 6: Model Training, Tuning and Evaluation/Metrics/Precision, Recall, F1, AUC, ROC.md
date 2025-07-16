# Model Evaluation Metrics – AWS MLE-A Exam

## ✅ Answering Strategy (Cheat-Sheet Style)

### 🎯 Precision
- Look for: **"Minimise false positives"**
- Use case: Email spam detection, fraud alerts (wrong positive is costly)

### 🎯 Recall
- Look for: **"Minimise false negatives"**
- Use case: Disease detection, safety alerts (missing a positive is dangerous)

### 🎯 F1 Score
- Look for: **"Balance between precision and recall"** or **"Imbalanced classes"**
- Use when both FP and FN are important and data is skewed

### 🎯 AUC / ROC
- Look for: **"Ranking classifier performance"**, **"Discrimination ability"**, **"Across thresholds"**
- Use when evaluating binary classifiers, especially with imbalanced datasets

## 🧠 Tips for the Exam

- If you see "imbalanced dataset" → **prefer F1 score or AUC**
- If cost of false **positive** is high → **precision**
- If cost of false **negative** is high → **recall**
- ROC curve plots **True Positive Rate vs False Positive Rate**
- AUC closer to **1.0 = better**, closer to **0.5 = random guessing**
- Don’t pick accuracy unless class balance is clearly stated
- Be careful with tricky wording — always map it back to which type of error matters more

## 📌 When NOT to use accuracy
- Class imbalance
- Cost-sensitive applications
- Binary rare-event classification
