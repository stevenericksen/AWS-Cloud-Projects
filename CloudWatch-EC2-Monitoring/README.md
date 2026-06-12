# EC2 Instance State Change Monitoring with CloudWatch & SNS

## Overview
Built a real-time monitoring solution that automatically notifies administrators when an EC2 instance changes state using Amazon EventBridge, SNS, and EC2.

## Services Used
- Amazon EC2
- Amazon SNS (Simple Notification Service)
- Amazon EventBridge (CloudWatch Events)

## What I Built
- Launched an EC2 instance (Amazon Linux 2023, t2.micro) in us-east-1
- Created an SNS topic with email subscription for notifications
- Configured an EventBridge rule to monitor EC2 instance state changes
- Tested the solution by stopping the EC2 instance and confirming email notification was received

## Walkthrough

### 1. EC2 Instance Running
![EC2 Running](01-EC2-Instance-Running.png)

### 2. SNS Topic Created
![SNS Topic](02-SNS-Topic-Created.png)

### 3. SNS Subscription Pending
![SNS Pending](03-SNS-Subscription-Pending.png)

### 4. Subscription Confirmation Email
![Email Confirmation](04-SNS-Subscription-Confirmation-Email.png)

### 5. Subscription Confirmed
![SNS Confirmed](05-SNS-Subscription-Confirmed.png)

### 6. EventBridge Rule Created
![EventBridge Rule](06-EventBridge-EC2RuleChange-Enabled.png)

### 7. EC2 Instance Stopping
![EC2 Stopping](07-EC2-Instance-Stopping.png)

### 8. EC2 Instance Stopped
![EC2 Stopped](08-EC2-Instance-Stopped.png)

### 9. AWS Notification Email Received
![AWS Notification](09-AWS-Notification-EC2-State-Change.png)

### 10. Lab Validation Passed 100%
![Validation](10-Whizlabs-Validation-Passed.png)

## Skills Demonstrated
- Cloud monitoring and alerting
- Event-driven architecture
- AWS Console navigation
- SNS topic and subscription configuration
- EventBridge rule creation
