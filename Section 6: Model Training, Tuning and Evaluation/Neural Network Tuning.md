# Neural Network Tuning – AWS MLE-A Exam

## 🔧 Learning Rate

| Setting      | Effect                                  |
|--------------|------------------------------------------|
| Too High     | Overshoots optimal point (unstable)      |
| Too Low      | Slower convergence (longer training)     |

- Controls **how big each update step** is during gradient descent.

## 📦 Batch Size

| Setting        | Effect                                                  |
|----------------|----------------------------------------------------------|
| Small          | Escapes local minima better, adds useful training noise  |
| Large          | Can get stuck in bad minima, inconsistent results        |

- Controls **how many samples** are used per training step.

## 🧪 Key Tips

- Both are **hyperparameters** — must be tuned.
- Small batch + balanced learning rate = better generalisation.
- Watch for inconsistent accuracy when batch size is too large.
