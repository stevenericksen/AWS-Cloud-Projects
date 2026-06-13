# VPC Flow Logs with Amazon Athena

## Overview
Built a complete AWS network monitoring pipeline that captures VPC traffic, stores flow logs in S3, and enables SQL-based log analysis using Amazon Athena.

## Services Used
- Amazon VPC
- Amazon S3
- Amazon EC2
- Amazon Athena
- VPC Flow Logs

## What I Built
- Created an S3 bucket with a log delivery bucket policy for VPC Flow Logs
- Built a custom VPC (10.0.0.0/16) with public subnet, Internet Gateway, and route table
- Configured VPC Flow Logs to capture all traffic at 1-minute intervals to S3
- Launched an EC2 instance (Amazon Linux 2023, t2.micro) and installed Apache HTTPD to generate traffic
- Created an Athena external table mapped to the S3 flow log path
- Ran SQL queries against live VPC flow log data returning source/destination IPs and actions
- Passed all lab validation checks at 100%

## Walkthrough

### 1. S3 Bucket Policy Editor
<img src="07_bucket-policy-editor.png" width="1000"/>

### 2. S3 Bucket Policy Saved
<img src="01_s3-bucket-policy.png" width="1000"/>

### 3. Create VPC Configuration
<img src="08_create-vpc-config.png" width="1000"/>

### 4. VPC Created
<img src="02_vpc-created.png" width="1000"/>

### 5. Internet Gateway Attached
<img src="03_igw-attached.png" width="1000"/>

### 6. Public Subnet Created
<img src="06_public-subnet.png" width="1000"/>

### 7. Subnet Association
<img src="05_subnet-association.png" width="1000"/>

### 8. Route Table with IGW Route
<img src="04_route-table-igw.png" width="1000"/>

### 9. Flow Log S3 Configuration
<img src="13_flowlog-s3-config.png" width="1000"/>

### 10. VPC Flow Log Active
<img src="12_vpc-flowlog-active.png" width="1000"/>

### 11. AWSLogs Folder in S3
<img src="16_s3-awslogs-folder.png" width="1000"/>

### 12. EC2 Instance Running
<img src="14_ec2-instance-running.png" width="1000"/>

### 13. SSH into EC2
<img src="15_ssh-ec2-terminal.png" width="1000"/>

### 14. Athena Query Results
<img src="10_athena-query-results.png" width="1000"/>

### 15. Athena Results Detail
<img src="11_athena-results-detail.png" width="1000"/>

### 16. Lab Validation Passed 100%
<img src="09_lab-validation-passed.png" width="1000"/>

## Skills Demonstrated
- VPC design and network architecture
- S3 bucket policy configuration for AWS log delivery
- VPC Flow Log setup and S3 integration
- EC2 provisioning and SSH access
- Amazon Athena external table creation
- SQL querying of live network flow log data
- End-to-end cloud observability pipeline
