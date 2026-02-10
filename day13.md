# Day 13: Top 15 AWS Services for DevOps Engineers

## 📖 Project Overview
As a DevOps engineer, navigating the 200+ services offered by AWS can be overwhelming. On Day 13, we shifted from manual deployment to understanding the core ecosystem. The goal was to identify and define the top 15 AWS services that are essential for building, securing, and monitoring infrastructure in a DevOps environment.

---

## 🏗️ The AWS Service Landscape

AWS operates on a service model (IaaS & PaaS), providing managed solutions that improve **Automation** and **Efficiency**. Instead of managing underlying hardware, we leverage these services to scale applications seamlessly.

---

## 🛠️ The Top 15 Essential Services

### 1. Compute & Networking
* **EC2 (Elastic Compute Cloud):** Virtual servers for running applications [00:04:24].
* **VPC (Virtual Private Cloud):** A private network for your resources, covering security groups, subnets, and traffic rules [00:05:00].
* **Lambda:** Serverless compute for executing short-lived functions and automated tasks without managing servers [00:15:35].

### 2. Storage & Database
* **EBS (Elastic Block Store):** Block storage volumes attached to EC2 instances for persistent data [00:06:52].
* **S3 (Simple Storage Service):** Scalable object storage for files, logs, and backups; now encrypted by default [00:08:01].

### 3. Identity & Security
* **IAM (Identity and Access Management):** Managing users, roles, and granular permissions [00:10:28].
* **KMS (Key Management Service):** Securely managing encryption keys for services like S3 and EBS [00:26:24].
* **CloudTrail:** Auditing service that records all API activity and logs actions for compliance [00:28:12].

### 4. Continuous Integration & Delivery (CI/CD)
* **CodePipeline:** Orchestrates the workflow of your CI/CD process [00:20:24].
* **CodeBuild:** A fully managed service that compiles code, runs tests, and produces artifacts [00:20:35].
* **CodeDeploy:** Automates code deployments to EC2, Fargate, or on-premises servers [00:20:46].

### 5. Monitoring & Governance
* **CloudWatch:** The primary monitoring and observability service for logs, metrics, and alarms [00:12:56].
* **AWS Config:** A guardrail service to track resource configurations and ensure compliance [00:24:43].
* **Billing & Cost Management:** Essential for tracking organization spending and optimizing costs [00:25:30].

### 6. Containers & Orchestration
* **EKS (Elastic Kubernetes Service):** Managed Kubernetes service for container orchestration [00:30:05].
* **ECS (Elastic Container Service):** AWS-proprietary container orchestration (alternative to Kubernetes) [00:31:16].

---

## 🔍 Key Comparison: EKS vs. ECS
| Feature | EKS (Elastic Kubernetes Service) | ECS (Elastic Container Service) |
| :--- | :--- | :--- |
| **Type** | Managed Kubernetes [00:30:42] | AWS Proprietary Solution [00:31:51] |
| **Complexity** | Higher (standard K8s APIs) | Lower (AWS-native integration) |
| **Portability** | High (Multi-cloud friendly) | Locked to AWS ecosystem |

---

## 🎯 Final Thoughts
A DevOps engineer doesn't need to know every single one of the 200+ AWS services. By mastering these 15 core services—specifically **IAM** for security, **VPC** for networking, and **Code Pipeline** for automation—you can manage almost any production-grade infrastructure.

---
[⬅️ Day 12](./day12.md) | [Main README](../README.md)
