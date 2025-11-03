# Confusion Matrix – AWS MLE-A Exam

## 🧠 Purpose

- Visual tool to understand **classification performance** beyond simple accuracy.
- Highlights **true/false positives/negatives**.

## 🔍 Key Terms (Binary)

| Actual \ Predicted | Yes (Positive) | No (Negative) |
|--------------------|----------------|---------------|
| Yes (Positive)     | True Positive  | False Negative|
| No (Negative)      | False Positive | True Negative |

- **TP + TN** = model got it right.
- **FP + FN** = model got it wrong.

## 🖼️ Variants

- **Multi-class confusion matrix**: Same concept, but with >2 labels.
- **Heatmap**: Darker colour = higher count.
- **Legacy AWS style**: May include **F1 scores** and **frequency totals** by row/column.

## ⚠️ Exam Tips

- **Always check axis labels** — placement of actual vs predicted is not consistent.
- High numbers on the **diagonal** = good performance.
- Use confusion matrix when **class imbalance** makes accuracy misleading.
