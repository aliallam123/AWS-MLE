# 🧠 KNN (K-Nearest Neighbors)
| Aspect                | What to Know                                                         |
| --------------------- | -------------------------------------------------------------------- |
| **Type**              | **Supervised** – Classification & Regression                         |
| **Input Format**      | `CSV` (label first) or `RecordIO-Protobuf`                           |
| **Input Mode**        | `File` or `Pipe`                                                     |
| **Preprocessing**     | Optional dimensionality reduction (SageMaker does this)              |
| **Core Idea**         | Predict label/value by averaging or voting over **K closest** points |
| **Key Hyperparams**   | `k` (number of neighbors), `sample_size`                             |
| **Instance Support**  | CPU: `ml.m5.2xlarge` or GPU: `ml.p2.xlarge`                          |
| **Use Cases**         | Simple classification, regression, or recommendation problems        |
| **Bonus (SageMaker)** | Builds an index + uses sampling to scale up KNN                      |

