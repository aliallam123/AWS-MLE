# 🛠️ Troubleshooting Amazon Kinesis Data Stream – Common Issues & Fixes

These are high-yield issues and fixes for the **AWS Machine Learning Engineer – Associate** exam. Expect scenario-based questions!

---

## 🚨 Producer Issues

### 📉 Writing is Too Slow
- Check for **throttling errors** and **service limits** (shard-level for reads/writes).
- Some API operations (e.g. `CreateStream`, `ListStreams`) have limits: **5–20 calls/sec**.
- Distribute load with **partition keys** evenly across shards.

### 🏗️ Large Producers
- Use **Kinesis Producer Library (KPL)** or batch/aggregate records with `PutRecords`.

### 📱 Small Producers
- Use `PutRecords` or **Kinesis Recorder (mobile SDK)**.

---

## ❌ Other Producer Errors

### 🔁 500 or 503 Errors
- Indicates `AmazonKinesisException` with error rate > **1%**
- ✅ **Retry with backoff**

### 🔗 Flink Connection Errors
- Check **network**, **Flink resource limits**, or **VPC misconfig**.

### ⏳ Timeout from Flink
- Tune `RequestTimeout` and `#setQueueLimit` on FlinkKinesisProducer.

### ⚠️ Throttling
- Check **hot shards** using enhanced monitoring.
- Try random partition keys to balance traffic.
- Enable **rate limiting** and **exponential backoff**.

---

## 👀 Consumer Issues

### ⚠️ Skipped Records (KCL)
- Check for unhandled exceptions in `processRecords`.

### 👯 Duplicate Processing in a Shard
- Happens if more than one processor is assigned.
- Adjust **failover time** and shutdown with reason `ZOMBIE`.

### 🐢 Reading Is Slow
- Add **shards**.
- Increase `maxRecords` per call.
- Optimise slow processor code.

### 😶 Empty `GetRecords` Responses
- Normal – just **keep polling**.

### 🕒 Shard Iterator Expiry
- You may need more **write capacity** in DynamoDB.

### 🐌 Falling Behind in Processing
- Monitor `IteratorAgeMilliseconds` and `MillisBehindLatest`.
- Extend **retention period** if needed.
- May be due to **insufficient resources**.

---

## 🧪 Lambda Consumer Issues

### ❌ Lambda Can’t Be Invoked
- Check **IAM permissions** on execution role.
- May be **timeout** or **concurrency breach**.
- Monitor `IteratorAge` for signs of lag.

### 🧵 `ReadProvisionedThroughputExceeded` Exception
- Caused by **throttling**.
- Fixes:
  - Reshard your stream
  - Use enhanced **fan-out**
  - Lower `GetRecords` size
  - Enable **retry with backoff**

---

## 🐌 General Consumer Performance

### 🚨 High Latency
- Monitor `GetRecords.Latency` & `IteratorAge`.
- Scale **shards**, raise **retention period**.
- Check **CPU/memory** (scale if needed).

### ❗️ 500 Errors
- Same as producers – **retry if >1%** error rate.

### 🧱 Blocked/Stuck KCL App
- Optimise `processRecords`.
- Raise `maxLeasesPerWorker`.
- Enable **KCL debug logs**.

---

📌 **Tip:** Kinesis issues often relate to **limits, resource scaling, retry logic, or IAM configs**. Know these cold for the exam!
