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

## 🧠 Tips

- Dropout commonly used in CNNs (e.g. 50% rate).
- Early stopping = practical, fast way to regularise.
- If training accuracy >> validation/test accuracy → overfitting!
