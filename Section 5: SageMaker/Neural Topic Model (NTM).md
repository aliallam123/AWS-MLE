# 🧠 Do I need to know this?
Yes — NTM is a built-in SageMaker algorithm for unsupervised topic modelling. It’s likely to show up on the exam, especially in questions about document clustering or unsupervised NLP.

# ✅ Exam-Focused Key Points
| Concept                   | What to Remember                                            |
| ------------------------- | ----------------------------------------------------------- |
| **Type**                  | Unsupervised learning – **Topic modelling**                 |
| **Goal**                  | Group documents by **latent topics** based on word patterns |
| **Use Cases**             | Document summarisation, search indexing, text clustering    |
| **Input Format**          | `CSV` or `RecordIO-Protobuf`                                |
| **Preprocessing**         | Requires:                                                   |
|                           | - **Tokenised word counts (integers)**                      |
|                           | - **Vocabulary file** (auxiliary channel)                   |
| **Input Mode**            | `File` or `Pipe` mode (pipe = faster)                       |
| **Main Hyperparameter**   | `num_topics` (how many topics to generate)                  |
| **Other Hyperparameters** | `batch_size`, `learning_rate`                               |
| **Output**                | Latent topics (not human-labelled) + top words per topic    |
| **Backend**               | Neural Variational Inference (deep learning)                |
| **Training**              | Use **GPU** recommended (but CPU also supported)            |
| **Inference**             | **CPU** usually sufficient                                  |


📝 Exam Tip
If the question mentions clustering documents by topic without labels, or latent topics, it’s Neural Topic Model (NTM).
You must pre-tokenise words into integers and supply a vocabulary file.
