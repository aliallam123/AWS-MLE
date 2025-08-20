# Amazon CloudWatch Metrics – AWS MLE-A Notes

## Key Concepts
- **Metrics** = Variables to monitor (e.g., EC2 CPUUtilization, S3 bucket size).  
- **Namespaces** = Each service has its own metric namespace.  
- **Dimensions** = Attributes of a metric (e.g., instance ID, environment). Max 30 per metric.  
- **Timestamps** = All metrics are time-based.

## Monitoring Granularity
- **Standard Monitoring** = 5-minute intervals.  
- **Detailed Monitoring** = 1-minute intervals.  

## Custom Metrics
- Used when AWS does not provide built-in metrics.  
- Example: EC2 memory usage.  

## Dashboards
- Visualise multiple metrics together.  

## Streaming Metrics
- Stream CloudWatch Metrics → **Kinesis Data Firehose**.  
- From Firehose, data can be sent to:  
  - **Amazon S3** (query with Athena)  
  - **Amazon Redshift** (warehousing)  
  - **Amazon OpenSearch** (dashboards/analytics)  
- Supports filtering by namespaces before streaming.  

---
