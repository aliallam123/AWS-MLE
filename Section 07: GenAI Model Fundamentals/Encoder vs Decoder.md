# 🧠 Encoder vs Decoder – Quick Revision

## 🎓 Analogy: Classroom Translator

- **Encoder** = The **Listener**  
  Listens to a sentence (e.g. in French) and understands the meaning.  
  👉 *"Je suis fatigué"* → internal meaning: “They’re tired.”

- **Decoder** = The **Speaker**  
  Takes that meaning and generates a response (e.g. in English).  
  👉 Says: “They’re tired.”

---

## 🔍 Transformer Breakdown

| Feature         | Encoder                          | Decoder                          |
|----------------|----------------------------------|----------------------------------|
| **Role**        | Understands the **input**        | Generates the **output**         |
| **Used in**     | BERT                             | GPT                              |
| **Input**       | Full input sequence              | Previous tokens (and encoder output if used) |
| **Attention**   | Self-attention only              | Self-attention + cross-attention |
| **Output**      | Embeddings/hidden states         | Tokens, one-by-one               |

---

## 🧪 Key Difference

- **Encoder**: Reads and encodes information into a **vector representation**.
- **Decoder**: Takes that representation and **generates new sequences** (e.g. words or tokens).

---

## 🤖 Model Examples

| Model | Uses | Architecture |
|-------|------|--------------|
| **BERT** | Classification, Q&A | Encoder-only |
| **GPT** | Text generation      | Decoder-only |
| **T5**  | Translation, summarisation | Encoder + Decoder |

