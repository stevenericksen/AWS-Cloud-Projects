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
![Bucket Policy Editor](07_bucket-policy-editor.png)

### 2. S3 Bucket Policy Saved
![Bucket Policy Saved](01_s3-bucket-policy.png)

### 3. Create VPC Configuration
![Create VPC](08_create-vpc-config.png)

### 4. VPC Created
![VPC Created](02_vpc-created.png)

### 5. Internet Gateway Attached
![IGW Attached](03_igw-attached.png)

### 6. Public Subnet Created
![Public Subnet](06_public-subnet.png)

### 7. Subnet Association
![Subnet Association](05_subnet-association.png)

### 8. Route Table with IGW Route
![Route Table](04_route-table-igw.png)

### 9. Flow Log S3 Configuration
![Flow Log Config](13_flowlog-s3-config.png)

### 10. VPC Flow Log Active
![Flow Log Active](12_vpc-flowlog-active.png)

### 11. AWSLogs Folder in S3
![AWSLogs Folder](16_s3-awslogs-folder.png)

### 12. EC2 Instance Running
![EC2 Running](14_ec2-instance-running.png)

### 13. SSH into EC2
![SSH Terminal](15_ssh-ec2-terminal.png)

### 14. Athena Query Results
![Athena Query](10_athena-query-results.png)

### 15. Athena Results Detail
![Athena Detail](11_athena-results-detail.png)

### 16. Lab Validation Passed 100%
![Validation](09_lab-validation-passed.png)

## Skills Demonstrated
- VPC design and network architecture
- S3 bucket policy configuration for AWS log delivery
- VPC Flow Log setup and S3 integration
- EC2 provisioning and SSH access
- Amazon Athena external table creation
- SQL querying of live network flow log data
- End-to-end cloud observability pipeline
