# 📘 SageMaker Built-in Algorithm: Object2Vec (Exam Revision)

## ✅ Overview
- **Type**: Deep learning embedding algorithm (general-purpose)
- **Use Cases**:
  - Similar item retrieval (recommender systems)
  - Similar user/item prediction
  - Genre prediction, clustering, nearest neighbour analysis
- Works with **arbitrary objects**, not just words (unlike Word2Vec)
- Learns **low-dimensional embeddings** from **pairs** of inputs

---

## 🧠 Core Concepts
- Learns relationships between **pairs of tokens/sequences**
  - Examples: user–item, product–description, sentence–label
- Each input has its own **encoder** path
- Encoders feed into a **comparator**, followed by a **feedforward NN**

---

## 📥 Input Format
- Inputs must be **tokenised as integer sequences**
- Each sample = **pair of tokens/sequences**
- Examples:
  - `[user_id], [item_id]`
  - `[genre_id], [description_tokens]`
- Two input channels (encoder1 & encoder2), paired for training

---

## ⚙️ Encoders
Choose per input channel:
- `average_pooling`
- `cnn`
- `bidirectional_lstm`

---

## 🎛️ Important Hyperparameters

### General DL Tuning
- `epochs`
- `batch_size`
- `learning_rate`
- `dropout`
- `early_stopping`
- `num_layers`
- `activation_function`
- `optimizer`
- `weight_decay`

### Encoder Setup
- `encoder_network_1`
- `encoder_network_2`

---

## 💻 Instance Support

### Training
- ✅ Single machine only (multi-GPU supported)
- ✅ CPU or GPU
- Recommended instances:
  - **CPU (default)**: `ml.m5.2xlarge`
  - **GPU (default)**: `ml.p2.xlarge`
  - **Larger jobs**:
    - CPU: `ml.m5.4xlarge` / `ml.m5.12xlarge`
    - GPU: `ml.p2`, `ml.p3`, `ml.g4`, `ml.g5`

### Inference
- ✅ Supports GPU inference
- Recommended: `ml.p3.2xlarge`
- Use environment variable: `inference_preferred_mode` to optimise for embeddings (vs classification)

---

## 📝 Exam Tips
- Use for **general embedding tasks** on object pairs
- Input = **integer token pairs** (not raw text or images)
- Can use **different encoders** per input
- **Multi-GPU supported on one machine**, but no multi-instance training
- Good fit for **recommender systems**, **similarity search**, and **clustering**
