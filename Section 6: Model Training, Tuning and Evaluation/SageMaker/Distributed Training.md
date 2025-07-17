# 🧠 SageMaker Distributed Training – GitHub Revision Notes

## 🧩 Types of Parallelism

- **Job Parallelism**: Running multiple independent training jobs in parallel.
- **Distributed Data Parallelism (DDP)**:
  - Split data across multiple GPUs/nodes.
  - Each GPU processes a portion of the data.
- **Model Parallelism**:
  - Split a single model across multiple devices.
  - Needed when model is too large to fit on one GPU.

---

## 🏗️ Best Practices Before Scaling Out

- Max out **GPU usage on a single instance** before scaling to multi-node.
- Example: use `ml.p4d.24xlarge` (8 GPUs) before scaling across instances.
- More efficient and cheaper than spreading across nodes too early.

---

## 🔁 SageMaker Distributed Training Libraries

- Built on AWS Custom Collective Comm Lib (like MapReduce for gradient updates).
- **AllReduce**:
  - Distributes and aggregates gradients during backpropagation.
- **AllGather**:
  - Offloads communication to CPU to reduce GPU load.

### How to Use
- Set `smdistributed` as backend in PyTorch estimator.
- Use `smdistributed.dataparallel` in distribution config.
- **Not compatible with Training Compiler**.

---

## 🛠️ Other Distributed Frameworks

- **PyTorch DDP**: Use `pytorchddp` in SageMaker.
- **TorchRun**: Use `torch_distributed`.
- **MPI (mpirun)**: Common for HPC setups.
- **Deepspeed**: Microsoft-backed, PyTorch only.
- **Horovod**: Open-source, supports multiple frameworks (e.g. TensorFlow, PyTorch).

---

## 💡 Exam Tips

- Know **AllReduce** = gradients
- Know **AllGather** = communications
- Know the difference between job, data, and model parallelism
- SageMaker DDP = more AWS-native, but others (Horovod, Deepspeed) also valid
