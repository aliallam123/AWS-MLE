# L1 vs L2 Regularization – AWS MLE-A Exam

## 🎯 Purpose

Reduce overfitting by penalizing large weights during training.

## 🔍 Key Differences

| Aspect         | L1 (Lasso)                          | L2 (Ridge)                         |
|----------------|-------------------------------------|------------------------------------|
| Penalty        | Sum of absolute weights             | Sum of squared weights             |
| Output         | Sparse (some weights = 0)           | Dense (no weights = 0)             |
| Use Case       | Feature selection                   | Keep all features, shrink weights  |
| Performance    | Computationally heavier             | More efficient                     |

## 🧠 Tips

- Use **L1** when you want **fewer features** → automatic feature selection.
- Use **L2** when all features are important → just reduce overfitting.
- Both can be combined (ElasticNet) — not exam-critical.
