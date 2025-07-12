# 📘 SageMaker Built-in Algorithm: BlazingText (Exam Revision)

## ✅ Overview
- **Type**: NLP (Natural Language Processing)
- **Use Cases**:
  - **Text Classification** (supervised)
  - **Word2Vec** (unsupervised word embeddings)
- ❗ Not for full documents — supports **sentences only**

---

## 🧠 Modes of Operation

### 🔹 Supervised Mode (Text Classification)
- Learns to classify sentences based on labelled training data
- Use Case: tagging, info retrieval, search relevance

### 🔹 Word2Vec Mode (Embedding Layer)
- Learns **word similarities** via embeddings
- Useful in downstream tasks (e.g., sentiment, translation)
- Cannot classify — only provides word vectors

#### Word2Vec Training Modes:
| Mode            | Notes                                                             |
|-----------------|-------------------------------------------------------------------|
| `cbow`          | Continuous bag of words – word order ignored                      |
| `skipgram`      | Order matters; works with n-grams                                 |
| `batch_skipgram`| Scalable across multiple CPU instances (no GPU)                   |

---

## 📥 Input Formats

### 🔹 Text Classification
- One sentence per line
- First "word" must be: `__label__<label>`
- Sentence must be:
  - Lowercased
  - Tokenised (space-separated, incl. punctuation)

**Example**:
__label__4 linux ready for prime time .


### 🔹 Word2Vec
- One sentence per line
- No labels
- Plain text

### 🔹 Augmented Manifest Format
- Structured JSON-style: `"source"` and `"label"` fields

---

## 🎛️ Important Hyperparameters

### Text Classification
- `learning_rate`
- `epochs`
- `word_ngrams`: how many words to look at together
- `vector_dim`: size of embedding vector

### Word2Vec
- `mode`: `cbow`, `skipgram`, or `batch_skipgram`
- `learning_rate`
- `window_size`: context window
- `vector_dim`
- `negative_samples`

---

## 💻 Instance Support

| Mode             | Instance Recommendation                        |
|------------------|------------------------------------------------|
| **cbow / skipgram**   | P3 (single machine GPU)                       |
| **batch_skipgram**    | Multiple CPU instances (scales horizontally) |
| **Text Classification** | 
- `<2GB data`: `ml.c5.xlarge`  
- `>2GB data`: `ml.p2.xlarge` or `ml.p3.2xlarge`

---

## 📝 Exam Tips
- **Supervised mode** → text classification
- **Word2Vec mode** → embedding only, NOT classification
- `batch_skipgram` → scales with CPUs across instances
- Know the **input formats** – especially `__label__` for classification
- Use **CBOW** when word order doesn’t matter, **skipgram** when it does
- Small training set? → use `c5` CPU
- Embedding mode? → use `P3` for best performance (except batch mode)
