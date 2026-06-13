# VPC Flow Logs with Amazon Athena

## Overview
This lab demonstrates building a complete AWS network monitoring pipeline — from VPC architecture through traffic generation to log analysis using SQL queries in Amazon Athena.

**Duration:** ~1 hour  
**Region:** US East (N. Virginia) us-east-1

---

## Architecture
- S3 Bucket (log destination with IAM delivery policy)
- Custom VPC with public subnet, Internet Gateway, and route table
- VPC Flow Logs → S3
- EC2 Instance (Amazon Linux 2023, t2.micro) generating HTTP traffic
- Amazon Athena querying flow log data via SQL

---

## Tasks Completed

| # | Task |
|---|------|
| 1 | Created S3 bucket with log delivery bucket policy |
| 2 | Created custom VPC (10.0.0.0/16) |
| 3 | Created and attached Internet Gateway |
| 4 | Created public subnet (10.0.1.0/24) with auto-assign public IP |
| 5 | Configured public route table with 0.0.0.0/0 → IGW route |
| 6 | Created VPC Flow Log (All traffic, 1-min interval, S3 destination) |
| 7 | Launched EC2 instance into custom VPC/subnet |
| 8 | SSH'd into EC2 and installed Apache HTTPD to generate traffic |
| 9 | Verified AWSLogs folder populated in S3 |
| 10 | Created Athena external table mapped to flow log S3 path |
| 11 | Ran SQL query returning 10 rows of parsed flow log data |
| 12 | Passed all lab validation checks (100%) |

---

## Screenshots

### S3 Bucket & Bucket Policy
<img src="07_bucket-policy-editor.png" width="800"/>
<img src="01_s3-bucket-policy.png" width="800"/>

### VPC Configuration
<img src="08_create-vpc-config.png" width="800"/>
<img src="02_vpc-created.png" width="800"/>
<img src="03_igw-attached.png" width="800"/>
<img src="06_public-subnet.png" width="800"/>
<img src="05_subnet-association.png" width="800"/>
<img src="04_route-table-igw.png" width="800"/>

### VPC Flow Logs
<img src="13_flowlog-s3-config.png" width="800"/>
<img src="12_vpc-flowlog-active.png" width="800"/>
<img src="16_s3-awslogs-folder.png" width="800"/>

### EC2 & Traffic Generation
<img src="14_ec2-instance-running.png" width="800"/>
<img src="15_ssh-ec2-terminal.png" width="800"/>

### Athena Query & Results
<img src="10_athena-query-results.png" width="800"/>
<img src="11_athena-results-detail.png" width="800"/>

### Validation
<img src="09_lab-validation-passed.png" width="800"/>

---

## Key Skills Demonstrated
- VPC design and networking (subnets, IGW, route tables)
- S3 bucket policy configuration for AWS log delivery
- VPC Flow Log setup and S3 integration
- EC2 provisioning and SSH access
- Amazon Athena external table creation and SQL querying
- End-to-end cloud observability pipeline
