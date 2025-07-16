# Advanced SageMaker AMT – AWS MLE-A Exam

## 🧠 Key Features

### 🔹 Early Stopping
- Stops training jobs **if no improvement** in objective metric
- Works only for models that emit metrics **each epoch**
- Enable by setting `early_stopping_type = 'Auto'`

### 🔹 Warm Start
- Reuses previous tuning jobs to speed up convergence
- Two modes:
  - **IdenticalDataAndAlgorithm** → same data/algorithm
  - **TransferLearning** → allows data variation

## 🛠️ Tuning Strategies

| Strategy       | Description                                              | Notes                                    |
|----------------|----------------------------------------------------------|------------------------------------------|
| Grid Search    | Tries **all combos** (categorical only)                  | Very expensive, not scalable             |
| Random Search  | Tries **random combos**                                  | Parallelisable, fast but less optimal    |
| Bayesian       | Learns & **improves each run** (regression-based)        | Sequential (limited parallelism)         |
| Hyperband      | Early stops bad configs, auto-parallel                   | **Best choice for deep learning**, fast  |

## 📏 Best Practices

- 🔢 Tune **few hyperparameters at a time**
- 📉 Use **small value ranges** where possible
- 🧮 Use **log scale** for values like learning rate (0.001–0.1)
- 🚫 **Don’t run too many jobs concurrently** — reduces AMT’s ability to learn

## ⛔ Resource Limits

- Default quotas:
  - Max parallel jobs
  - Max training jobs per tuning job
  - Max hyperparameters
- 📩 Increase via **AWS support request** if needed

## 🧪 Exam Tips

- If you see “stopped early” → answer is **early stopping**
- If using **previous jobs to restart** tuning → answer is **warm start**
- For **deep learning models** + **epoch metrics** → use **Hyperband**
- If parallelism is key → use **random search**
- If you want **best convergence** and can run sequentially → use **Bayesian**
