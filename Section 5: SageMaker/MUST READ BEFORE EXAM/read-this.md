# 📘 What You Need to Know About SageMaker Algorithms (MLE-A Exam)

| **What You’re Tested On**              | **Examples / Notes**                                                           |
| -------------------------------------- | ------------------------------------------------------------------------------ |
| ✅ **What the algorithm is for**        | E.g., *“Which algorithm is best for dimensionality reduction?” → PCA*          |
| ✅ **Supervised vs Unsupervised**       | E.g., KNN = Supervised, K-Means = Unsupervised                                 |
| ✅ **Key strength / use case**          | E.g., *“Sparse recommender system?” → Factorization Machines*                  |
| ✅ **Basic input format expectations**  | Just whether it’s CSV, RecordIO, or both (don’t need full syntax)              |
| ✅ **Main hyperparameter(s)**           | 1–2 important ones only (e.g., `k` for KNN/K-Means, `num_factors` for FM)      |
| ✅ **Instance preference (CPU vs GPU)** | Especially if GPU is **required** or **pointless** (e.g., FM = CPU, CNN = GPU) |
| ✅ **What kind of output it gives**     | E.g., Object Detection = labels + bounding boxes, PCA = components             |
| ❌ Input mode (file/pipe)               | **Rarely tested** unless it's a performance-specific question                  |
| ❌ Full hyperparameter lists            | Only core ones are relevant                                                    |
| ❌ Internal algorithm details           | No maths or code — just conceptual application                                 |


# 🧠 How to Think in the Exam
If the question says:

“How to reduce features before training?” → PCA

“How to cluster users without labels?” → K-Means

“Which supervised algorithm works well with sparse data?” → Factorization Machines

“You want to classify objects in images.” → Image Classification

“You want to detect objects and where they are in an image.” → Object Detection

“Which algorithm groups docs by latent topics?” → NTM or LDA

“Which one returns a mask for every pixel?” → Semantic Segmentation

# ✅ Your Study Strategy
Learn what each algorithm does

Learn why/when to use it

Remember 1–2 key hyperparameters (max)

Know if it needs GPU or can use CPU
