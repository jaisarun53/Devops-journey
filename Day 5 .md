# 🛠️ Day 5: AWS CLI, SSH, and Automation Walkthrough

## 📖 Overview
On Day 5, we moved away from the "Point-and-Click" method (UI) to the "Command-Line" method. We learned how to securely log into our servers and how to configure our local machines to talk to the AWS Cloud directly via the terminal.

---

## 🔑 1. Connecting to your VM (SSH & Terminal)
Once a Virtual Machine (EC2) is running, you need a way to send it instructions.

### Methods of Connection:
* **EC2 Instance Connect (UI):** A quick, browser-based terminal provided by AWS.
* **SSH (Secure Shell):** The industry-standard way to connect from your local terminal.
    * **Command:** `ssh -i "your-key.pem" ubuntu@your-public-ip`
    * **Permission Fix:** If you see a "Permissions are too open" error, run:
        ```bash
        chmod 400 your-key.pem
        ```

### Recommended Terminals:
* **Mac:** iTerm2
* **Windows:** MobaXterm (highly recommended for beginners), Putty, or Git Bash.

---

## ⚡ 2. AWS CLI (Command Line Interface)
The AWS CLI allows you to manage your entire cloud infrastructure using commands instead of the web dashboard.

### Setup Process:
1.  **Download & Install:** Install the AWS CLI binary for your OS.
2.  **Verify Installation:** Run `aws --version`.
3.  **Security Credentials:** * Go to **IAM** -> **Security Credentials** in AWS.
    * Create an **Access Key** and **Secret Access Key**.
4.  **Configuration:** Run `aws configure` and enter your keys, default region (e.g., `us-east-1`), and output format (`json`).

### Common Commands:
* **List S3 Buckets:** `aws s3 ls`
* **Create S3 Bucket:** `aws s3 mb s3://unique-bucket-name`
* **List Instances:** `aws ec2 describe-instances`

---

## 🤖 3. Introduction to Automation & IaC
We briefly explored how professionals avoid manual work:
* **AWS CloudFormation (CFT):** Using YAML/JSON templates to define infrastructure.
* **Boto3:** A Python library that allows you to write scripts to control AWS.
* **Infrastructure as Code (IaC):** The concept that your hardware setup should be written in code (like Terraform), which we will dive into later in the course.

---

## 💡 Key Takeaways
* **Identity File (PEM):** This is a secret key; if you lose it, you lose access to your server.
* **Public vs. Private IP:** Always use the **Public IP** to connect from your home/office laptop.
* **CLI Efficiency:** The CLI is much faster than the UI for repetitive tasks like listing or deleting multiple resources.

---

## 🔗 Resources
* **Video Reference:** [Day 5 - AWS CLI Full Guide](https://www.youtube.com/watch?v=cN4pt5KQ9eA)
* **Docs:** [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/reference/)

---
[⬅️ Back to Main README](./README.md)
