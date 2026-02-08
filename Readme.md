# AWS VPC Flow Logs – Hands-on Implementation

## 📌 Project Overview
This project demonstrates the implementation of **AWS VPC Flow Logs** to monitor and analyze network traffic within an AWS Virtual Private Cloud (VPC).

The objective of this hands-on exercise is to understand how network traffic flows between resources in public and private subnets and how VPC Flow Logs help in troubleshooting, monitoring, and improving security visibility.

---

## 🏗️ Architecture Overview

The architecture includes:

- Custom VPC
- Public Subnet
- Private Subnet
- Internet Gateway
- NAT Gateway
- Route Tables
- EC2 Instances
- VPC Flow Logs
- CloudWatch Log Group

### Architecture Diagram
![VPC Flow Logs Architecture](./images/vpc-flowlogs-architecture.png)

---

## ⚙️ Services Used

- Amazon VPC
- Amazon EC2
- Internet Gateway
- NAT Gateway
- Amazon CloudWatch
- VPC Flow Logs

---

## 🎯 Objectives

- Create a custom VPC with CIDR block
- Configure public and private subnets
- Enable internet access using Internet Gateway
- Configure outbound internet access using NAT Gateway
- Launch EC2 instances in both subnets
- Enable VPC Flow Logs
- Send logs to CloudWatch Log Group
- Analyze ACCEPT and REJECT traffic logs

---

## 🧩 Implementation Steps

### 1️⃣ Create VPC
- Created a VPC with CIDR block `12.0.0.0/24`

### 2️⃣ Create Subnets
- Public Subnet: `12.0.1.0/24`
- Private Subnet: `12.0.2.0/24`

### 3️⃣ Configure Internet Gateway
- Attached Internet Gateway to VPC
- Updated route table for public subnet

### 4️⃣ Configure NAT Gateway
- Created NAT Gateway in public subnet
- Updated private subnet route table for internet access

### 5️⃣ Launch EC2 Instances
- EC2 instance in public subnet
- EC2 instance in private subnet

### 6️⃣ Enable VPC Flow Logs
- Enabled flow logs at VPC level
- Selected CloudWatch Log Group as destination
- Configured IAM role for logging permissions

---

## 📊 Flow Log Details

VPC Flow Logs capture:

- Source IP
- Destination IP
- Source Port
- Destination Port
- Protocol
- Traffic status (ACCEPT / REJECT)
- Bytes transferred
- Timestamp

> Note: Flow logs capture metadata only, not actual packet content.

---

## ✅ Learning Outcomes

- Understanding of AWS VPC networking
- Network traffic monitoring using Flow Logs
- Troubleshooting connectivity issues
- CloudWatch log analysis
- Practical exposure to cloud networking concepts

---

## 📷 Screenshots

Screenshots of configuration and logs are available in the `/images` folder.

---

## 🔗 Author

**Vipul Pandey**  
System Admin | Cloud & DevOps & Linux Learner

---

## 📌 Future Improvements

- Flow log analysis using CloudWatch Insights
- Integration with S3 for long-term log storage
- Automated monitoring and alerts

