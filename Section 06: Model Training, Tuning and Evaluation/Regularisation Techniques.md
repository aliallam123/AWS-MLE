# Regularization Techniques – AWS MLE-A Exam

## 🎯 Goal

Prevent **overfitting**: when model performs well on training data but poorly on validation/test data.

## 🧪 Key Techniques

| Technique        | Description                                                  |
|------------------|--------------------------------------------------------------|
| Model Simplification | Reduce neurons/layers to limit model complexity             |
| Dropout          | Randomly disables neurons during training to avoid memorisation |
| Early Stopping   | Halts training when validation performance stops improving   |

## 📊 Data Splits

- **Training set**: Used to train the model.
- **Validation set**: Used to monitor performance during training.
- **Test set**: Used to evaluate model after training is complete.

  # 🧠 Story Summary: Regularization
Imagine training a student (your neural network). If they memorise the textbook (training data), they ace practice tests but fail real exams — that’s overfitting.

You want the student to generalise — so you:

Simplify the material (simpler model),

Randomly hide notes during study (dropout),

Stop when their performance plateaus (early stopping).

Regularization techniques are those tricks — they prevent overfitting and help your model perform better on unseen data (test/eval sets), not just training examples.

## 🧠 Tips

- Dropout commonly used in CNNs (e.g. 50% rate).
- Early stopping = practical, fast way to regularise.
- If training accuracy >> validation/test accuracy → overfitting!
