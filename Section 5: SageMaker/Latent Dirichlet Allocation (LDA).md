# 🧠 Do I need to know this?
Yes — LDA is the second built-in topic modelling algorithm in SageMaker and may be tested in contrast to Neural Topic Model (NTM).

# ✅ Exam-Focused Key Points

| Concept                  | What to Remember                                                   |
| ------------------------ | ------------------------------------------------------------------ |
| **Type**                 | Unsupervised topic modelling                                       |
| **Model Type**           | **Non-deep learning** (Bayesian-based generative model)            |
| **Use Cases**            | Clustering documents, customer segmentation, music analysis        |
| **Input Format**         | `CSV` or `RecordIO-Protobuf`                                       |
| **Preprocessing**        | Tokenise text into **word count vectors** + **vocabulary mapping** |
| **Input Mode**           | `File` or `Pipe` (Pipe mode only works with RecordIO)              |
| **Output**               | Document–topic distributions, not human-readable labels            |
| **Main Hyperparameter**  | `num_topics` – controls granularity of clustering                  |
| **Other Hyperparameter** | `alpha0`: controls topic sparsity                                  |
| **Evaluation Metric**    | `per_word_log_likelihood`                                          |
| **Training**             | **CPU only**, **single instance only**                             |
| **Inference**            | Can run on CPU, efficient and low-cost                             |


# 🔁 Comparison to Neural Topic Model (NTM)

| Feature        | **LDA**                | **NTM**                          |
| -------------- | ---------------------- | -------------------------------- |
| Algorithm Type | Bayesian (non-neural)  | Neural (deep learning)           |
| Backend        | CPU-only               | GPU or CPU                       |
| Training Scope | Single instance only   | Scalable with GPU                |
| Hyperparams    | `num_topics`, `alpha0` | `num_topics`, `batch_size`, `lr` |
| Output         | Topic distributions    | Latent vector topics             |

# 📝 Exam Tip
If you see unsupervised clustering using a non-neural algorithm that runs on CPU only, it’s LDA.
Remember: Pipe mode only with RecordIO, and the main tuning knob is num_topics.
