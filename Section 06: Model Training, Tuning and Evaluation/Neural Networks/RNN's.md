# Recurrent Neural Networks (RNNs) – AWS MLE-A Exam

## 🔁 Purpose

- RNNs handle **sequential** data: time series, text, music, trajectories.
- Retain memory via loops — past inputs affect future predictions.

## ⚙️ Key Concepts

| Concept         | Description                                           |
|-----------------|-------------------------------------------------------|
| Unrolling       | Treats each time step like a layer during training    |
| BPTT            | Backpropagation Through Time – updates across steps   |
| Truncated BPTT  | Limits time steps to reduce compute cost              |
| Tanh            | Typical activation function for smooth memory flow    |

## 🧠 Advanced Cells

| Cell | Use Case                         | Notes                                |
|------|----------------------------------|--------------------------------------|
| LSTM | Retains both long & short memory | Use when older inputs matter          |
| GRU  | Simplified LSTM                  | Faster, good trade-off                |

## 🧪 Topologies

| Type       | Example Use Case                    |
|------------|-------------------------------------|
| Seq2Seq    | Translation, music continuation     |
| Seq2Vec    | Sentiment from sentence             |
| Vec2Seq    | Image → caption                     |

## 🧠 Tips

- Use **LSTM or GRU** over vanilla RNNs for long sequences.
- Use **GRU** for faster training with near-LSTM accuracy.
- Use **tanh** activations to maintain smooth gradients.
