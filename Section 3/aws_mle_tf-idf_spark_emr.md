
# 🧠 AWS MLE Associate Exam: TF-IDF + Spark + EMR Studio (Revision Notes)

---

## 📌 1. What is TF-IDF?

**TF-IDF = Term Frequency × Inverse Document Frequency**

Used to measure how important a word is to a document in a collection. Common in **search engines** and **text analysis**.

| Term | Meaning | Example |
|------|---------|---------|
| **TF (Term Frequency)** | How often a word appears in a doc | "machine" appears 10 times |
| **IDF (Inverse Doc Frequency)** | How rare the word is across all docs | "machine" is rare, "the" is common |
| **TF-IDF Score** | TF × IDF | High = word is important for that doc |

---

## 📚 2. Why is TF-IDF in the AWS MLE-A Course?

It's part of the **"Data Preparation for ML" (28%)** exam domain.

- Teaches **text feature engineering**
- Shows **preprocessing at scale** using **Spark + EMR**
- Involves creating **unigrams, bigrams (n-grams)** for NLP
- Demonstrates using **PySpark + Jupyter (EMR Studio)** for real-world data prep

---

## 🧪 3. TF-IDF Example Use Case

### Use Case:
- Index many documents (e.g. Wikipedia pages, books)
- User types a search term (like "love")
- TF-IDF ranks which docs are most relevant
- Docs with highest score are shown first

### Bonus:
Can use **unigrams**, **bigrams**, **trigrams** (n-grams) to capture phrases:
- Example: “I love AWS” → bigrams = `["I love", "love AWS"]`

---

## 💻 4. What is EMR Studio?

> ✅ Just a **Jupyter notebook** connected to a **Spark cluster on AWS**

| Feature | EMR Studio |
|---------|------------|
| Editor | Jupyter Notebook |
| Backend | Spark cluster on EMR |
| Benefit | Scalable processing for large datasets |
| Use Case | TF-IDF on massive corpora like Wikipedia |

---

## ⚡ 5. Why Spark (on EMR) over regular Python?

| Feature | Local Python | Spark on EMR |
|--------|---------------|--------------|
| Data size | Small | Massive (TBs) |
| Speed | Slower | Distributed + faster |
| Memory | Limited | Shared across nodes |
| Parallelism | No | Yes (auto-scaling) |
| Tools | pandas, scikit-learn | PySpark, MLlib |

### So yes:
> You *can* run TF-IDF locally with `TfidfVectorizer`, **but** EMR + Spark is better for production or big data use cases.

---

## 🛠 6. Can I Use PySpark Locally?

✅ Yes, but with setup:

- Install Java + Spark + PySpark
- Run Spark in **local mode**
- Use Jupyter + SparkSession

> But it won't scale like AWS EMR — still great for learning!

---

## 🌐 7. AWS Services That Offer Spark

- **Amazon EMR** – fully managed Spark clusters
- **EMR Studio** – Jupyter UI to interact with Spark
- **SageMaker Notebooks** – can support Spark kernels
- **Glue** – another option for serverless Spark

---

## 📌 Summary

TF-IDF is:
- A text feature engineering tool 📊
- Exam-relevant for **data prep + NLP**
- Best run at scale using **Apache Spark**
- Easily handled in AWS via **EMR + EMR Studio**

---

📝 **Pro Tip**: Expect exam questions on:
- When to use EMR for data prep
- How Spark handles n-grams or TF-IDF at scale
- Choosing tools like `Spark on EMR` vs `Glue` or `Data Wrangler`

