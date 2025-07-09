# 🧠 What to Know:
When using AWS Glue DataBrew, you should be able to handle PII (Personally Identifiable Information) using built-in transformations like:

| Technique                    | Purpose                                                     |
| ---------------------------- | ----------------------------------------------------------- |
| **Substitution**             | Replace PII with random values                              |
| **Shuffling**                | Mix PII values across rows (⚠️ not safe for sensitive data) |
| **Deterministic Encryption** | Same input → same encrypted output                          |
| **Probabilistic Encryption** | Same input → different outputs each time                    |
| **Hashing**                  | Irreversible transformation for anonymisation               |
| **Masking**                  | Obscure part of value (e.g. `****1234`)                     |
| **Deletion / Nulling**       | Remove PII fields entirely                                  |


🎯 Exam Tip:
Know which transformation method fits which use case, especially for PII compliance and anonymization in data preparation workflows.
