# SageMaker Model Monitor

## 🐶 What Is Model Monitor?

- Automatically monitors **deployed models** for:
  - **Data drift**
  - **Model quality drift**
  - **Bias drift**
  - **Feature attribution drift**

- Integrated with **CloudWatch** for real-time alerts.
- **No-code setup** via SageMaker Studio dashboard.
- Results stored in **S3**; can be visualised in:
  - TensorBoard
  - QuickSight
  - Tableau

## 🧠 Monitoring Types

| Monitoring Type           | Description                                                              |
|---------------------------|--------------------------------------------------------------------------|
| **Data Quality Drift**    | Changes in input data stats (mean, std, min/max). Compared to baseline. |
| **Model Quality Drift**   | Drops in metrics like accuracy, RMSE, precision, recall.                |
| **Bias Drift**            | Detected via **SageMaker Clarify** across groups (e.g., income, age).    |
| **Feature Attribution Drift** | Changes in feature importance ranking. Uses **nDCG** metric.         |

## ⚙️ Setup & Integration

- Define a **monitoring schedule** to run checks periodically.
- **Baselines required** for both:
  - Data quality monitoring
  - Model quality monitoring
- Supports **ground truth integration** to compare model output with human labels.

## ✅ Exam Essentials

- Monitors deployed models for **drift, bias, quality, and attribution**.
- Works with **CloudWatch** for alerting.
- **nDCG** is used for detecting **feature attribution drift**.
- Set up monitoring jobs via schedule; store results in **S3**.
- Integrates with **Clarify** to catch **new or emerging bias**.

## 🎯 Quick Tips

- If it watches your live model = **Model Monitor**.
- Mentions “new feature appeared”, “bias drift” = Model Monitor + Clarify.
- Feature importance changed? → Check **nDCG** for attribution drift.
