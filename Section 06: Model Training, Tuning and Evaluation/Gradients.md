# Vanishing & Exploding Gradients – AWS MLE-A Exam

## ⚠️ Problems

| Type               | Description                                   | Effect                      |
|--------------------|-----------------------------------------------|-----------------------------|
| Vanishing Gradient | Gradients → 0 in deep layers                   | Model stops learning        |
| Exploding Gradient | Gradients too large → unstable updates        | Model breaks/diverges       |

## 🛠️ Fixes for Vanishing Gradients

- Use **ReLU** activation
- Use **LSTM** (RNNs) or **ResNet** (CNNs)
- Train in **layered hierarchy**, not all at once

## 🔍 Gradient Checking

- Verifies gradient computations during training
- Mostly used in **low-level debugging** or research

# 🧠 Story Summary: Vanishing/Exploding Gradients
Imagine you're rolling a ball down a hill to find the lowest point (training a model).

As you reach the bottom, the slope flattens — it's hard to tell where to go. That's the vanishing gradient — tiny updates, slow or stalled learning.

At the top, the slope is too steep — the ball flies out of control. That's the exploding gradient — unstable learning.

These problems happen especially in deep networks and RNNs. Solutions? Use ReLU, split networks into smaller blocks, or use special architectures like LSTM or ResNet.
Also, gradient checking is like debugging your math — just to make sure your code is computing those slopes correctly.
