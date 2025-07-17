# 🚀 Advanced SageMaker Training Techniques – GitHub Revision Notes

## 🔧 SageMaker Training Compiler (Deprecated but exam-relevant)

- **Purpose**: Auto-compiles and optimises training jobs for GPU performance (up to 50% faster).
- **Integrated with**: AWS Deep Learning Containers (DLC) only – not Bring Your Own Container (BYOC).
- **Frameworks**: PyTorch (preferably with PyTorch XLA models), TensorFlow, MXNet.
- **How to use**:
  - Use `compiler_config=TrainingCompilerConfig()` in the estimator.
  - Enable debugging via `debug=True` in config.
- **Requirements**:
  - GPU instances (P3, P4, G4, G5).
- **Limitations**:
  - Not maintained anymore.
  - Not compatible with SageMaker Distributed Training Libraries.

---

## 🔁 Warm Pools

- **Purpose**: Keep hardware & data “warm” between training jobs to reduce cold start time.
- **Use case**: Frequent/repeated training jobs.
- **How to enable**:
  - Set `keep_alive_period_in_seconds` in training job’s resource config (via SDK or SageMaker UI).
  - Must submit a **service limit increase** request to use.
- **Also features**: Persistent cache to retain data across runs.

---

## 💡 Exam Traps to Avoid

- Don’t assume Training Compiler is still actively developed—**it's deprecated**.
- You **can’t use** Training Compiler with custom containers or distributed libraries.
- Warm Pools **require a service limit increase**—don’t forget that if asked in a scenario.
