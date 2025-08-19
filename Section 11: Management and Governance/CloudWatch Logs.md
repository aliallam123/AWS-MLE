# Amazon CloudWatch Logs – AWS MLE-A Notes

## Key Concepts
- **Log Groups**: Containers for logs (usually one per application).  
- **Log Streams**: Individual instances/files/containers within a group.  
- **Retention**: Configurable (1 day → 10 years, or indefinite).  
- **Encryption**: Enabled by default, can use KMS CMKs.

## Sources of Logs
- **AWS services**: Lambda, ECS, Elastic Beanstalk, API Gateway, VPC Flow Logs, Route53, CloudTrail.  
- **Agents**: CloudWatch Unified Agent (preferred over old Logs Agent).  
- **Custom**: SDKs to push application logs.

## Querying Logs
- **CloudWatch Logs Insights**: Purpose-built query language.  
  - Queries historical data (not real-time).  
  - Supports filtering, aggregates, statistics, sorting.  
  - Results can be visualised or added to Dashboards.  
  - Supports multiple log groups and even cross-account queries.

## Exporting & Streaming
- **Batch Export**: CreateExportTask → Amazon S3 (delayed, up to 12 hours).  
- **Real-Time Streaming**:  
  - Subscription Filters → Kinesis Data Streams / Kinesis Firehose / Lambda / OpenSearch.  
  - Can filter events before sending.  
  - Supports **cross-account log aggregation** via Destinations + IAM roles.

---
