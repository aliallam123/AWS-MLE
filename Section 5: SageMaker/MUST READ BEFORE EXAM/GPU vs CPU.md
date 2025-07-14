# 🔥 Must-Know GPU vs CPU Scenarios (for the Exam)

| Algorithm                    | **GPU Required?**    | **What to Remember**                                             |
| ---------------------------- | -------------------- | ---------------------------------------------------------------- |
| **Image Classification**     | ✅ Yes                | Deep learning = use GPU (P2/P3/G4/G5)                            |
| **Object Detection**         | ✅ Yes                | Uses CNN + SSD — GPU needed for training                         |
| **Semantic Segmentation**    | ✅ Yes                | Pixel-wise deep learning — GPU **only** for training             |
| **Seq2Seq**                  | ✅ Yes                | Very GPU-intensive (use P3), **single-machine only**             |
| **Neural Topic Model (NTM)** | ✅ Preferred          | Neural net = GPU preferred, but CPU OK for inference             |
| **Factorization Machines**   | ❌ No                 | Use **CPU** — GPU not helpful for sparse data                    |
| **K-Means**                  | ❌ No (CPU preferred) | Can use GPU, but only **1 GPU per instance** — CPU scales better |
| **KNN**                      | ❌ No (CPU preferred) | GPU optional — good for large batch inference throughput         |
| **PCA**                      | ❌ No (Either)        | GPU or CPU — try both based on data size                         |
| **LDA**                      | ❌ No                 | CPU **only**, **single-instance only**                           |
| **BlazingText**              | ⚠️ Depends           | Text classification → CPU or GPU                                 |
| Word2Vec (skipgram) → GPU    |                      |                                                                  |
| Batch skipgram → multi-CPU   |                      |                                                                  |


# 🎓 TL;DR
If it’s deep learning or image-heavy → GPU ✅

If it’s sparse data or clustering → CPU ✅

If it only works on one machine → may limit scaling/GPU benefit
