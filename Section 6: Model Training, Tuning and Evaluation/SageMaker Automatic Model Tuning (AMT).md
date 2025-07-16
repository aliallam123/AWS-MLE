# SageMaker Automatic Model Tuning (AMT) – AWS MLE-A Exam

## 🧠 What It Is

- SageMaker AMT automates **hyperparameter tuning** using parallel training jobs
- Learns over time → uses **Bayesian optimisation**, not brute-force grid search
- Trains multiple models with different hyperparameter combos to **optimise a metric**

## 🎯 Key Best Practices

| Practice                        | Why it matters                                      |
|---------------------------------|-----------------------------------------------------|
| ✅ Limit hyperparameters         | Too many → exponential cost & time                  |
| ✅ Use small search ranges       | Large ranges → wasted resources                     |
| ✅ Use **log scale** when needed | For values like learning rate (e.g. 0.001–0.1)      |
| ✅ Keep concurrent jobs low      | Learning works better **sequentially**              |
| ✅ Report correct metric         | Needed if using custom training scripts             |

## 🚀 Answer Clues for the Exam

- If question says **“efficient tuning”** → choose **Bayesian** or **SageMaker AMT**
- If question asks how to **reduce cost/time** → tune fewer hyperparams, use small ranges
- If question says **parallel tuning isn't working well** → reduce concurrency
- Log scale = good for **learning rate**, **regularisation**, etc.
- Grid/random search = **less efficient** than AMT

## 🧪 Common Traps

- Don’t tune 5+ hyperparameters at once
- Don’t allow full concurrency if learning-as-you-go is expected
- Don’t use linear scale for parameters ranging over **multiple orders of magnitude**
