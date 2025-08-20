# AWS X-Ray – AWS MLE-A Notes

## Key Concepts
- **Purpose**: Distributed tracing service → debug, analyze performance, and find bottlenecks in microservice architectures.  
- **Service Map**: Visual diagram showing how requests flow across services (e.g., EC2 → API Gateway → DynamoDB).  
- **Traces**: End-to-end record of a request.  
  - **Segments** = Components in the request path.  
  - **Subsegments** = Smaller operations within a segment.  
  - **Annotations** = Extra metadata added to traces.  

## Benefits
- 🔎 Identify **bottlenecks** and performance issues.  
- 🗺️ Understand **dependencies** in distributed systems.  
- ⏱️ Check if requests meet **SLA latency goals**.  
- 👤 Pinpoint **which users** are impacted by errors.  
- 🖼️ Graphical → non-technical teams can help troubleshoot.  

## Compatibility
- Works with **Lambda, Beanstalk, ECS, API Gateway, ELB, EC2**, and even on-prem servers.  
- Supports Java, Python, Go, Node.js, .NET.  

## How It Works
1. **Instrument code** with the X-Ray SDK (captures AWS SDK calls, DB queries, HTTP requests, etc.).  
2. **Daemon required** (except for Lambda and some managed services):  
   - EC2/on-prem → must install and run the **X-Ray Daemon** (intercepts traces and batches to AWS X-Ray every ~1s).  
   - Lambda → enable **Active Tracing** + ensure proper IAM role.  
3. **IAM permissions** needed for apps/services to write data to X-Ray.  
4. Collected traces → aggregated into the **service map**.  

## Security
- IAM controls access to X-Ray.  
- Encryption at rest with KMS supported.  

---

## 🔑 Exam Tips
- 🖼️ X-Ray gives a **visual service map** for debugging distributed apps.  
- ⚙️ **Daemon must run** on EC2/on-prem; Lambda handles this automatically.  
- 📦 **SDK instrumentation is required** to capture traces.  
- 🚨 Common exam trap: “X-Ray works locally but not on EC2” → **Daemon not running** or **IAM role missing**.  
- ⏱️ You can trace **all requests or sample a subset** (e.g., % of requests, 5 per minute).  

---
