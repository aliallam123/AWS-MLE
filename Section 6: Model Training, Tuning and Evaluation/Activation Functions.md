# Activation Functions – AWS MLE-A Exam

## 🔑 Purpose
Activation functions introduce **non-linearity**, enabling networks to learn complex patterns.

## ⚡ Common Functions & Use Cases

| Function | Range         | Use Case                                 | Notes                               |
|----------|---------------|------------------------------------------|-------------------------------------|
| ReLU     | 0 to ∞        | Default for hidden layers                | Fast, efficient, may suffer "dying" |
| Leaky ReLU | ~ -0.01 to ∞ | Fix for dying ReLU                       | Small negative slope                |
| PreLU    | Learned slope | Advanced fix for dying ReLU              | More compute needed                 |
| ELU      | Exp + linear  | Smooth alternative to Leaky ReLU         | Better derivatives                  |
| Sigmoid  | 0 to 1        | Multi-label output                       | Causes vanishing gradients          |
| Tanh     | -1 to 1       | Recurrent Neural Networks                | Zero-centred, still vanishing grad  |
| Softmax  | 0 to 1 (sum=1)| Multi-class classification output layer  | Converts logits to class probabilities |

## 🧪 Key Concepts

- **Vanishing Gradient**: Sigmoid/tanh saturate → gradients shrink → slow learning.
- **Dying ReLU**: Neurons stuck at 0 for all inputs.
- **Softmax vs Sigmoid**:
  - Use **Softmax** if output = **one class**.
  - Use **Sigmoid** if output = **multiple classes**.

## 🧠 Tips

- Start with **ReLU** for hidden layers.
- Use **Softmax** for multi-class classification (e.g. 1 label from 5).
- Use **Sigmoid** for multi-label classification (e.g. can be label 1 and 3).
- For RNNs, prefer **Tanh**.

