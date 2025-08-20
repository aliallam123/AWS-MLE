# Amazon CloudWatch Alarms – AWS MLE-A Notes

## Key Concepts
- **Alarms** monitor metrics and trigger actions when thresholds are breached.  
- **States**:  
  - ✅ OK – Threshold not breached.  
  - ❓ INSUFFICIENT_DATA – Not enough data.  
  - 🚨 ALARM – Threshold breached.  
- **Period**: Evaluation time window (can support high-resolution metrics like 10s, 30s, 60s).  

## Alarm Actions
- **EC2 instance actions**: Stop, terminate, reboot, or recover.  
- **Auto Scaling actions**: Trigger scale in/out.  
- **Notifications**: Send to SNS → Lambda, email, or other targets.  

## Composite Alarms
- Combine multiple alarms using **AND/OR logic**.  
- ✅ Reduces noise by alerting only when specific conditions across alarms are met.  
- Example: CPU high **AND** IOPS high → send notification.  

## EC2 Recovery
- Monitors:  
  - **Instance status check** (VM health).  
  - **System status check** (underlying hardware).  
  - **EBS status check** (volume health).  
- Recovery keeps **same private/public/elastic IPs, metadata, and placement group**.  

## Logs Integration
- **Metric Filters**: Convert CloudWatch Logs into metrics (e.g., count “ERROR” messages).  
- Alarms can then trigger on these metrics → useful for app monitoring.  

## Testing
- Use CLI `set-alarm-state` to simulate alarms and test notifications.  

---

## 🔑 Exam Tips
- 📊 Alarms are **metric-based**, while **Logs → Metric Filters → Alarms** allow log-based alerting.  
- 🔁 **Composite Alarms** = combine alarms with AND/OR to reduce noise.  
- 🛠️ **EC2 Recovery** keeps IPs/metadata – unlike stop/terminate/reboot.  
- 🚨 Always remember: Alarms trigger **SNS, EC2 actions, or Auto Scaling**.  
- 🧪 `set-alarm-state` = test alarms without waiting for thresholds.  

---
