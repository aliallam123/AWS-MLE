# 📊 PCA (Principal Component Analysis) — Exam Table

| **Aspect**              | **What to Know**                                                            |
| ----------------------- | --------------------------------------------------------------------------- |
| **Type**                | Unsupervised — Dimensionality Reduction                                     |
| **Goal**                | Reduce high-dimensional data into fewer components while retaining variance |
| **Input Format**        | `CSV` or `RecordIO-Protobuf`                                                |
| **Input Mode**          | `File` or `Pipe`                                                            |
| **Core Algorithm**      | Uses **Singular Value Decomposition (SVD)** on the **covariance matrix**    |
| **Main Use Case**       | Reduce features before training to avoid overfitting / improve performance  |
| **Key Hyperparameters** | `algorithm_mode` (`regular` or `randomized`), `subtract_mean`               |
| **Modes**               | `regular` → sparse/moderate data, `randomized` → large data                 |
| **Output**              | Top-N **principal components** (no labels, just dimensions)                 |
| **Instance Types**      | ✅ CPU or GPU supported (no fixed recommendation — try both)                |


# 🔥 What to Memorise for the Exam
PCA is used for dimensionality reduction, not prediction

It’s unsupervised, doesn’t require labels

Returns components, not feature names

SageMaker supports both regular and randomized modes

Hyperparams to know: algorithm_mode, subtract_mean

Can use GPU or CPU, depending on dataset size and sparsity

# ✅ Exam Clue:

If a question asks about reducing features or removing irrelevant dimensions, the answer is probably PCA.
