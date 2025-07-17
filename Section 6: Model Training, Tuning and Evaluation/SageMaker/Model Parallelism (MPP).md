# 🧠 SageMaker Model Parallelism (MPP) – GitHub Revision Notes

## 🧩 Why Use Model Parallelism?

- When **model size > GPU memory**
- Needed for **very large models** (e.g. >1B parameters)
- Goal: spread the model across multiple GPUs

---

## 🛠️ SageMaker Model Parallelism Library (MPP)

- **Framework**: PyTorch only
- **Current version**: v2 (simplified usage)

### Techniques Used

1. **Optimizer State Sharding**:
   - Splits model weights across GPUs
   - Requires **stateful optimizers** (e.g. Adam, FP16)
   - Effective for >1B parameter models

2. **Activation Checkpointing**:
   - Saves memory by **not storing activations**
   - Recomputes them during backpropagation (trades compute for memory)

3. **Activation Offloading**:
   - Moves checkpointed activations between **CPU and GPU**
   - Reduces GPU memory usage

---

## ⚙️ How to Use MPP

- Import: `import torch_sagemaker as tsm`
- Set distribution config:
  ```python
  distribution = {
      "smdistributed": {
          "modelparallel": {
              "enabled": True,
              ...
          }
      }
  }
