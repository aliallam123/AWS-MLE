| Aspect                  | What to Know                                                                  |
| ----------------------- | ----------------------------------------------------------------------------- |
| **Type**                | **Unsupervised** – Clustering                                                 |
| **Input Format**        | `CSV` or `RecordIO-Protobuf`                                                  |
| **Input Mode**          | `File` or `Pipe`                                                              |
| **Core Idea**           | Finds **K cluster centers** in feature space                                  |
| **Sharding (Exam Tip)** | For training: use `ShardedByS3Key`                                            |
| **Testing (optional)**  | Use `FullyReplicated` when testing                                            |
| **Key Hyperparams**     | `k`, `extra_cluster_center_factor`, `init_method`, `mini_batch_size`          |
| **Init Options**        | `random` or `kmeans++` (SageMaker default)                                    |
| **Instance Support**    | CPU preferred, or GPU: `ml.g4dn.8xlarge` (1 GPU max per node)                 |
| **Bonus (SageMaker)**   | Uses **more initial clusters** (big K), reduced to `k` with Lloyd’s algorithm |
