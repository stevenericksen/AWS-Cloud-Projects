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

## Results
- Successfully received automated email notifications when EC2 instance state changed from running to stopping to stopped
- Validated end-to-end monitoring pipeline working in real time

## Screenshots
See screenshots folder for full walkthrough evidence

## Skills Demonstrated
- Cloud monitoring and alerting
- Event-driven architecture
- AWS Console navigation
- SNS topic and subscription configuration
- EventBridge rule creation
