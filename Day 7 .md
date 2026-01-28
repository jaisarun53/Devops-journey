# 🚀 Day 7: AWS Resource Tracker Shell Script Project

## 📖 Overview
In a cloud environment, organizations often waste money on unused resources. This project creates a shell script that audits an AWS account for S3 buckets, EC2 instances, Lambda functions, and IAM users.

---

## 🎯 Project Objective
Create a script that:
1.  Lists **S3 Buckets**.
2.  Lists **EC2 Instances** (specifically Instance IDs).
3.  Lists **Lambda Functions**.
4.  Lists **IAM Users**.
5.  Automates this process using a **Cron Job**.

---

## 🛠️ Prerequisites
* **AWS CLI:** Installed and configured (`aws configure`).
* **JQ:** A command-line JSON processor (Essential for parsing AWS CLI output).
    * *Install:* `sudo apt install jq`

---

## 📜 The Shell Script: `aws_resource_tracker.sh`

```bash
#!/bin/bash

########################################
# Author: Arun
# Date: 28th-Jan
# Version: v1
#
# This script will report the AWS resource usage
########################################

# Debug mode
set -x

# List S3 buckets
echo "Print list of s3 buckets"
aws s3 ls

# List EC2 Instances
echo "Print list of ec2 instances"
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId'

# List Lambda functions
echo "Print list of lambda functions"
aws lambda list-functions

# List IAM users
echo "Print list of IAM users"
aws iam list-users
