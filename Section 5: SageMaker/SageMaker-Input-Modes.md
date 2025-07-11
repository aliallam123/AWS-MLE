| **Input Mode / Storage** | **Best For**                             | **Key Traits**                           | **VPC Needed?** |
| ------------------------ | ---------------------------------------- | ---------------------------------------- | --------------- |
| **File Mode**            | Small data                               | Copies data to instance, simple          | ❌               |
| **Fast File Mode**       | Medium-large data, needs speed           | Streams from S3, supports random access  | ❌               |
| **Pipe Mode**            | Sequential streaming                     | Streams S3 data, no random access        | ❌               |
| **S3 Express One Zone**  | Speed boost (low-latency, same AZ)       | Speeds up File/FastFile/Pipe (1 AZ only) | ❌               |
| **FSx for Lustre**       | **Massive** data, high IOPS & throughput | Petabyte scale, very low latency         | ✅               |
| **Amazon EFS**           | Data already in EFS                      | Pull directly from EFS                   | ✅               |



🧠 Quick Tips:

Small data? → File Mode

Need speed? → Fast File Mode

Stream-only (simple)? → Pipe Mode

Crazy performance? → FSx for Lustre

Want to speed up any mode? → Use S3 Express One Zone

Using EFS already? → Use EFS
