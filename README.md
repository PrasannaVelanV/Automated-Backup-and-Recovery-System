# Automated Backup and Recovery System using AWS

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws)
![Lambda](https://img.shields.io/badge/AWS_Lambda-Serverless-FF9900?logo=awslambda)
![EC2](https://img.shields.io/badge/Amazon_EC2-Compute-orange?logo=amazonec2)
![EBS](https://img.shields.io/badge/Amazon_EBS-Block_Storage-blue)
![EventBridge](https://img.shields.io/badge/Amazon_EventBridge-Automation-purple)
![IAM](https://img.shields.io/badge/IAM-Security-red?logo=amazonaws)

# Automated Backup and Recovery System using AWS

## 📖 Project Overview

This project demonstrates a fully automated backup and recovery solution for Amazon EC2 Elastic Block Store (EBS) volumes using AWS serverless services.

The system automatically creates EBS snapshots on a scheduled basis and removes outdated snapshots based on a predefined retention policy. This ensures reliable backup management while optimizing storage costs and minimizing manual intervention.

The solution leverages **AWS Lambda**, **Amazon EventBridge**, **Amazon EC2**, **Amazon EBS**, and **IAM** to implement a secure, scalable, and cost-effective disaster recovery strategy.

---

## Architecture



![Architecture](https://raw.githubusercontent.com/PrasannaVelanV/Automated-Backup-and-Recovery-System/main/Architecture%20-%20Automated%20Backup%20and%20Recovery%20System.png)

---

## 🚀 Architecture Components

### Compute Layer

* Amazon EC2 Instance
* Amazon EBS Volume

### Automation Layer

* AWS Lambda Function
* Amazon EventBridge Scheduled Rule

### Security Layer

* IAM Roles and Policies

### Backup Layer

* Amazon EBS Snapshots

---

## 🛠️ AWS Services Used

| Service              | Purpose                                 |
| -------------------- | --------------------------------------- |
| Amazon EC2           | Hosts the application server            |
| Amazon EBS           | Provides persistent block storage       |
| AWS Lambda           | Automates backup and cleanup operations |
| Amazon EventBridge   | Triggers Lambda functions on a schedule |
| AWS IAM              | Manages secure permissions              |
| Amazon EBS Snapshots | Stores incremental backups              |

---

## ✨ Features

* Automated EBS snapshot creation
* Scheduled backup execution using EventBridge
* Snapshot retention policy implementation
* Automatic deletion of outdated snapshots
* Fully serverless architecture
* IAM-based secure access control
* Cost optimization through lifecycle management
* Disaster recovery readiness

---

## 🔄 Architecture Workflow

1. Amazon EventBridge triggers the AWS Lambda function on a scheduled interval.
2. Lambda identifies the target EC2 EBS volume.
3. A new EBS snapshot is created automatically.
4. Existing snapshots are evaluated against the retention policy.
5. Snapshots older than the configured retention period are deleted.
6. Recent snapshots remain available for backup and recovery purposes.

---

## 🎯 Project Scope

This project focuses on implementing an automated and cost-efficient backup solution for Amazon EC2 EBS volumes.

### Included

* Automated snapshot creation
* Snapshot lifecycle management
* Scheduled serverless execution
* IAM-based secure access control
* Backup automation using AWS Lambda

---

## 📈 Benefits

* Improved data protection
* Reduced manual administrative effort
* Lower storage costs
* Consistent backup scheduling
* Faster disaster recovery
* Increased operational efficiency

---

## 🔐 IAM Permissions

The Lambda execution role includes permissions for:

* Describe Volumes
* Describe Snapshots
* Create Snapshot
* Delete Snapshot
* Create Tags
* CloudWatch Logs access

---

## 📂 Project Structure

```bash
Automated-Backup-and-Recovery-System/
│
├── lambda_function.txt
├── README.md
├── Architecture - Automated Backup and Recovery System.png
├── Screenshots/
└── Automated-Backup-and-Recovery-System.pdf
```

---

## ⚙️ Deployment Workflow

### 1. Create an IAM Role

Grant the following permissions:

* EC2 Snapshot Management
* Describe Volumes
* Describe Snapshots
* CloudWatch Logs

### 2. Create a Lambda Function

* Upload the Python backup automation script.
* Attach the IAM execution role.

### 3. Configure EventBridge Rule

* Create a scheduled rule using cron or rate expressions.
* Configure the Lambda function as the target.

### 4. Test the Solution

* Trigger the Lambda function manually.
* Verify snapshot creation in the EC2 console.
* Confirm automatic deletion based on the retention policy.

---

## 🧠 Skills Demonstrated

* AWS Lambda
* Amazon EC2
* Amazon EBS
* Amazon EventBridge
* IAM Roles and Policies
* Python Automation
* Serverless Computing
* Backup and Recovery
* Disaster Recovery Planning
* Infrastructure Automation
* Cost Optimization

---

## 📚 Learning Outcomes

Through this project, I gained practical experience in:

* Designing automated backup solutions
* Implementing serverless workflows using AWS Lambda
* Scheduling automation using Amazon EventBridge
* Managing Amazon EBS snapshots programmatically
* Configuring IAM roles and permissions
* Applying AWS best practices for automation and cost optimization

---

## 🔮 Future Enhancements

* Email notifications using Amazon SNS
* Cross-region snapshot replication
* Multi-volume backup support
* Snapshot encryption using AWS KMS
* CloudWatch alarms and monitoring dashboards
* Backup reporting and analytics

---

## 🧹 Resource Cleanup

To avoid unnecessary AWS charges, delete the following resources when no longer needed:

```bash
- Lambda Function
- EventBridge Rule
- EBS Snapshots
- IAM Role
```

---

## 👨‍💻 Author

### Prasanna Velan

* GitHub: https://github.com/PrasannaVelanV
* LinkedIn: https://www.linkedin.com/in/prasanna-velan-v/
* Portfolio: https://prasannavelanv.netlify.app/

---

## ⭐ Support

If you found this project helpful, please consider giving this repository a ⭐ on GitHub.
