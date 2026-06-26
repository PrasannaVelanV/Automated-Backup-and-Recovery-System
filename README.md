# Automated Backup and Recovery System using AWS

## Project Overview

This project demonstrates an automated backup solution for Amazon EC2 Elastic Block Store (EBS) volumes using AWS serverless services. The system automatically creates EBS snapshots on a scheduled basis and removes outdated snapshots according to a defined retention policy, ensuring reliable backups while optimizing storage costs.

## Architecture

## Architecture

![Architecture](https://raw.githubusercontent.com/PrasannaVelanV/Automated-Backup-and-Recovery-System/main/Architecture%20-%20Automated%20Backup%20and%20Recovery%20System.png)
---

## Features

- Automated EBS snapshot creation
- Scheduled backup using Amazon EventBridge (CloudWatch Events)
- Snapshot retention policy
- Automatic deletion of expired snapshots
- Fully serverless automation using AWS Lambda
- IAM role-based secure access
- Cost optimization through lifecycle management

---

## AWS Services Used

| Service | Purpose |
|----------|---------|
| Amazon EC2 | Hosts the application server |
| Amazon EBS | Persistent block storage attached to EC2 |
| AWS Lambda | Automates snapshot creation and cleanup |
| Amazon EventBridge (CloudWatch Events) | Triggers Lambda on a schedule |
| AWS IAM | Provides secure permissions to Lambda |
| Amazon EBS Snapshots | Stores incremental backups |

---

## Architecture Workflow

1. Amazon EventBridge triggers the Lambda function based on a scheduled rule.
2. Lambda identifies the target EC2 EBS volume.
3. Lambda creates a new EBS snapshot.
4. Existing snapshots are checked.
5. Snapshots older than the configured retention period are deleted automatically.
6. Latest backups remain available for disaster recovery.

---

## Project Scope

This project focuses on implementing an automated backup solution for Amazon EC2 EBS volumes.

### Included

- Automated snapshot creation
- Snapshot retention management
- Scheduled execution
- IAM-based access control
- Backup automation

### Benefits

- Improved data protection
- Reduced manual effort
- Lower storage costs
- Consistent backup scheduling
- Faster disaster recovery

---

## IAM Permissions

The Lambda execution role includes permissions for:

- EC2 Snapshot Management
- Describe Volumes
- Describe Snapshots
- Create Snapshot
- Delete Snapshot
- CloudWatch Logs

---

## Folder Structure

```
Automated-Backup-and-Recovery-System/
│
├── lambda_function.py
├── README.md
├── Architecture - Automated Backup and Recovery System.png
├── Screenshots/
├── Automated-Backup-and-Recovery-System.pdf
```

---


## Skills Demonstrated

- AWS EC2
- Amazon EBS
- AWS Lambda
- Amazon EventBridge
- IAM Roles and Policies
- Python Automation
- Infrastructure Automation
- Backup & Recovery
- Disaster Recovery
- Cost Optimization

---

## Future Enhancements

- Email notifications using Amazon SNS
- Multi-volume backup support
- Cross-region snapshot replication
- Backup monitoring dashboard
- CloudWatch alarms
- Snapshot encryption using AWS KMS

---

## Learning Outcomes

Through this project, I gained practical experience in:

- Automating infrastructure tasks using AWS Lambda
- Implementing scheduled serverless workflows
- Managing Amazon EBS snapshots
- Designing backup and recovery strategies
- Configuring IAM roles and permissions
- Applying AWS best practices for automation and cost optimization

---

## Author

### Prasanna Velan

- GitHub: https://github.com/PrasannaVelanV
- LinkedIn: [www.linkedin.com/in/prasannavelanv](https://www.linkedin.com/in/prasanna-velan-v/)
- Portfolio: [https://github.com/PrasannaVelanV](https://prasannavelanv.netlify.app/)

---

## ⭐ Support

If you found this project helpful, please give this repository a ⭐ on GitHub.
