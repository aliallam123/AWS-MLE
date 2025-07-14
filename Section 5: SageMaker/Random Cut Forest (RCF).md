# 🧠 What to Know for the Exam
| Topic               | Key Info                                                            |
| ------------------- | ------------------------------------------------------------------- |
| **Purpose**         | Unsupervised **anomaly detection**                                  |
| **Input Format**    | `CSV` or `RecordIO-Protobuf`                                        |
| **Input Mode**      | Supports `File` or `Pipe` mode                                      |
| **Output**          | Assigns an **anomaly score** to each data point                     |
| **Test Channel**    | Optional — for precision/recall/F1 on labelled data                 |
| **Algorithm Type**  | Amazon-built algorithm based on **random partitioning forests**     |
| **How it works**    | Adds new data to trees → **big structural changes = anomaly**       |
| **Hyperparameters** | `num_trees`, `num_samples_per_tree` (tune based on anomaly ratio)   |
| **Use Cases**       | Works with **batch + streaming data** (e.g., via Kinesis Analytics) |
| **Instance Type**   | CPU-only: `ml.m4`, `ml.c4`, `ml.c5` (inference: `ml.c5.xlarge`)     |


# 🔥 Exam Clue
If the question is about unsupervised anomaly detection, especially streaming, RCF is your answer.
