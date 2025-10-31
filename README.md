# amazing-zone
AWS-project and more
---
## Goals

- Deploy a secure and scalable Aurora MySQL database
- Launch a web application on EC2
- Implement RDS Proxy for connection pooling
- Set up Blue/Green Deployment for safe DB upgrades
- Monitor infrastructure using CloudWatch

---

##  Technologies Used

- Amazon Aurora MySQL (v3)
- Amazon EC2 (Ubuntu or Amazon Linux)
- Amazon RDS Proxy
- Amazon S3 (optional for static assets)
- AWS IAM
- AWS CloudWatch
- AWS Systems Manager Parameter Store
- AWS VPC

---

## Setup Instructions

### 1. Create a VPC
- Public and private subnets
- Internet Gateway and route tables
- Enable DNS hostnames

### 2. Launch Aurora MySQL
- Go to RDS → Create Database
- Select Aurora MySQL v3 (MySQL 8.0)
- Enable RDS Proxy
- Place DB in private subnet

### 3. Deploy EC2 Instance
- Launch EC2 in public subnet
- Install web app (e.g., Flask, Node.js, or PHP)
- Configure security groups for HTTP and MySQL access

### 4. Connect EC2 to Aurora
- Use RDS Proxy endpoint in your app
- Store DB credentials in Parameter Store or Secrets Manager

### 5. Set Up Blue/Green Deployment
- In RDS Console → Create Blue/Green Deployment
- Test against green environment
- Switch traffic when ready

### 6. Enable Monitoring
- CloudWatch Logs for EC2 and RDS
- CloudWatch Alarms for CPU, memory, DB connections

---

##  Optional Enhancements

- S3 for backups or static assets
- Lambda for automation
- ALB for load balancing
- Auto Scaling Group for EC2

---

##  Learning Outcomes

- Understand Aurora MySQL provisioning and scaling
- Implement secure EC2-to-RDS connectivity
- Use RDS Proxy for efficient connection management
- Perform safe DB upgrades with Blue/Green Deployments
- Monitor and troubleshoot AWS infrastructure

---

## Resources

- [Aurora MySQL Documentation](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/AuroraMySQL.Reference.html)
- [RDS Proxy Setup](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html)
- [Blue/Green Deployments](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/blue-green-deployments.html)
- [CloudWatch Monitoring](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)

---

## Author

Taofeek Osipitan

This project was created to help AWS learners gain hands-on experience with database services and deployment strategies.

